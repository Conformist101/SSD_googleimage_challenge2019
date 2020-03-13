# SSD_googleimage_challenge2019
<h1><img src="https://pytorch.org/assets/images/ssd_diagram.png" /></h1>
<h1>Model Description</h1>
<h3>This SSD300 model is based on the SSD: Single Shot MultiBox Detector paper, which describes SSD as &ldquo;a method for detecting objects in images using a single deep neural network&rdquo;. The input size is fixed to 300x300.<a href="http://arxiv.org/abs/1512.02325">paper link</a></h3>
<h3>Additional enhancement:</h3>
<ul>
<li>The conv5_x, avgpool, fc and softmax layers were removed from the original classification model.</li>
<li>All strides in conv4_x are set to 1x1.</li>
</ul>
<p>The backbone is followed by 5 additional convolutional layers. In addition to the convolutional layers, we attached 6 detection heads:</p>
<ul>
<li>The first detection head is attached to the last conv4_x layer.</li>
<li>The other five detection heads are attached to the corresponding 5 additional layers.</li>
</ul>
<h4>The main difference between this model and the one described in the paper is in the backbone. Specifically, the VGG model is obsolete and is replaced by the ResNet-50 model.</h4>
<h4>Reference:&nbsp;<a href="https://pytorch.org/hub/nvidia_deeplearningexamples_ssd/">https://pytorch.org/hub/nvidia_deeplearningexamples_ssd/</a><a class="anchor-link" href="https://render.githubusercontent.com/view/ipynb?commit=898b3efbc5654fea5e5a49cbd2f3caa1d3a076b1&amp;enc_url=68747470733a2f2f7261772e67697468756275736572636f6e74656e742e636f6d2f436f6e666f726d6973743130312f5353445f676f6f676c65696d6167655f6368616c6c656e6765323031392f383938623365666263353635346665613565356134396362643266336361613164336130373662312f7373642d676f6f676c65696d6167652d6368616c6c656e6765323031392e6970796e62&amp;nwo=Conformist101%2FSSD_googleimage_challenge2019&amp;path=ssd-googleimage-challenge2019.ipynb&amp;repository_id=247042867&amp;repository_type=Repository#Reference:-https://pytorch.org/hub/nvidia_deeplearningexamples_ssd/">&para;</a></h4>
<p><strong>Dataset:&nbsp;<a title="Google open-images-2019-object-detection DataSet" href="https://www.kaggle.com/c/open-images-2019-object-detection">https://www.kaggle.com/c/open-images-2019-object-detection</a></strong></p>
<p><strong>Result:</strong></p>
<p><strong><img src="https://www.kaggleusercontent.com/kf/30108259/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..5ZLmcY_-gkxyDALc_kytmA.bcnV8RC37Z2yHl6Dl_X7hsN571b_8ZtnbrZd1Y1V0EKtK0Zw4fvtEBXP02d1KPQVxklFKAb8cLVNepfKlyfyZd2-TDv99jsOoBZQy9gOTKzo5iqLSsq1Q7f54d0b-PfdR5_j9CPpLwOBOiVmU5w-T7DM-gqk2ZFD1U-1ON9TRSs.Nq8YspEg76eIYH-pRuc1AA/__results___files/__results___24_0.png" alt="" width="267" height="252" /><img src="https://www.kaggleusercontent.com/kf/30108259/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..5ZLmcY_-gkxyDALc_kytmA.bcnV8RC37Z2yHl6Dl_X7hsN571b_8ZtnbrZd1Y1V0EKtK0Zw4fvtEBXP02d1KPQVxklFKAb8cLVNepfKlyfyZd2-TDv99jsOoBZQy9gOTKzo5iqLSsq1Q7f54d0b-PfdR5_j9CPpLwOBOiVmU5w-T7DM-gqk2ZFD1U-1ON9TRSs.Nq8YspEg76eIYH-pRuc1AA/__results___files/__results___24_1.png" alt="" width="267" height="252" /></strong></p>
<p><strong><img src="https://www.kaggleusercontent.com/kf/30108259/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..5ZLmcY_-gkxyDALc_kytmA.bcnV8RC37Z2yHl6Dl_X7hsN571b_8ZtnbrZd1Y1V0EKtK0Zw4fvtEBXP02d1KPQVxklFKAb8cLVNepfKlyfyZd2-TDv99jsOoBZQy9gOTKzo5iqLSsq1Q7f54d0b-PfdR5_j9CPpLwOBOiVmU5w-T7DM-gqk2ZFD1U-1ON9TRSs.Nq8YspEg76eIYH-pRuc1AA/__results___files/__results___24_3.png" alt="" width="288" height="252" /><img src="https://www.kaggleusercontent.com/kf/30108259/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..5ZLmcY_-gkxyDALc_kytmA.bcnV8RC37Z2yHl6Dl_X7hsN571b_8ZtnbrZd1Y1V0EKtK0Zw4fvtEBXP02d1KPQVxklFKAb8cLVNepfKlyfyZd2-TDv99jsOoBZQy9gOTKzo5iqLSsq1Q7f54d0b-PfdR5_j9CPpLwOBOiVmU5w-T7DM-gqk2ZFD1U-1ON9TRSs.Nq8YspEg76eIYH-pRuc1AA/__results___files/__results___24_4.png" alt="" width="267" height="252" /></strong></p>
<p><img src="https://www.kaggleusercontent.com/kf/30108259/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..5ZLmcY_-gkxyDALc_kytmA.bcnV8RC37Z2yHl6Dl_X7hsN571b_8ZtnbrZd1Y1V0EKtK0Zw4fvtEBXP02d1KPQVxklFKAb8cLVNepfKlyfyZd2-TDv99jsOoBZQy9gOTKzo5iqLSsq1Q7f54d0b-PfdR5_j9CPpLwOBOiVmU5w-T7DM-gqk2ZFD1U-1ON9TRSs.Nq8YspEg76eIYH-pRuc1AA/__results___files/__results___24_2.png" alt="" width="267" height="252" /></p>
