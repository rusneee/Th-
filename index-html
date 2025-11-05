<!doctype html>
<html lang="vi">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Phong Bì Thư Cổ Điển</title>
  <script src="/_sdk/element_sdk.js"></script>
  <script src="/_sdk/data_sdk.js"></script>
  <style>
    body {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      background: #f5f5f0;
      font-family: 'Georgia', serif;
      overflow: hidden;
    }

    html {
      height: 100%;
    }

    .container {
      width: 100%;
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      overflow: hidden;
    }

    .sparkles {
      position: absolute;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 1;
    }

    .sparkle {
      position: absolute;
      width: 4px;
      height: 4px;
      background: #ffd700;
      border-radius: 50%;
      animation: sparkleFloat 4s ease-in-out infinite;
      opacity: 0;
    }

    @keyframes sparkleFloat {
      0% { opacity: 0; transform: translateY(100px) scale(0); }
      20% { opacity: 1; transform: translateY(0px) scale(1); }
      80% { opacity: 1; transform: translateY(-20px) scale(1); }
      100% { opacity: 0; transform: translateY(-100px) scale(0); }
    }

    .sparkle:nth-child(1) { left: 10%; animation-delay: 0s; }
    .sparkle:nth-child(2) { left: 20%; animation-delay: 0.5s; }
    .sparkle:nth-child(3) { left: 30%; animation-delay: 1s; }
    .sparkle:nth-child(4) { left: 40%; animation-delay: 1.5s; }
    .sparkle:nth-child(5) { left: 50%; animation-delay: 2s; }
    .sparkle:nth-child(6) { left: 60%; animation-delay: 2.5s; }
    .sparkle:nth-child(7) { left: 70%; animation-delay: 3s; }
    .sparkle:nth-child(8) { left: 80%; animation-delay: 3.5s; }
    .sparkle:nth-child(9) { left: 90%; animation-delay: 4s; }
    .sparkle:nth-child(10) { left: 15%; animation-delay: 0.8s; }
    .sparkle:nth-child(11) { left: 35%; animation-delay: 1.3s; }
    .sparkle:nth-child(12) { left: 55%; animation-delay: 1.8s; }
    .sparkle:nth-child(13) { left: 75%; animation-delay: 2.3s; }
    .sparkle:nth-child(14) { left: 85%; animation-delay: 2.8s; }
    .sparkle:nth-child(15) { left: 25%; animation-delay: 3.3s; }

    .envelope-wrapper {
      position: relative;
      width: 500px;
      height: 320px;
      cursor: pointer;
      transition: transform 0.3s ease;
      animation: envelopeFloat 6s ease-in-out infinite;
      z-index: 2;
    }

    @keyframes envelopeFloat {
      0%, 100% { transform: translateY(0px) rotate(0deg); }
      25% { transform: translateY(-8px) rotate(0.5deg); }
      50% { transform: translateY(-5px) rotate(0deg); }
      75% { transform: translateY(-10px) rotate(-0.5deg); }
    }

    .envelope-wrapper:hover {
      transform: scale(1.05);
      animation-play-state: paused;
    }

    .envelope-wrapper.opening {
      pointer-events: none;
    }

    .envelope {
      position: relative;
      width: 100%;
      height: 100%;
      background: #f9f6f0;
      border: 2px solid #d4c5a9;
      box-shadow: 0 8px 30px rgba(0,0,0,0.2), inset 0 0 20px rgba(212,197,169,0.3);
    }

    .envelope-texture {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      opacity: 0.05;
      background-image: repeating-linear-gradient(45deg, transparent, transparent 2px, #8b7355 2px, #8b7355 4px);
      pointer-events: none;
    }

    .envelope-flap {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 160px;
      background: #ede4d3;
      border-bottom: 2px solid #d4c5a9;
      clip-path: polygon(0 0, 50% 100%, 100% 0);
      transform-origin: top center;
      transition: transform 1s ease;
      box-shadow: 0 4px 15px rgba(0,0,0,0.15);
      z-index: 3;
    }

    .envelope-wrapper.opening .envelope-flap {
      transform: rotateX(180deg);
    }

    .ribbon {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      z-index: 4;
      transition: opacity 0.5s ease, transform 0.8s ease;
    }

    .envelope-wrapper.opening .ribbon {
      opacity: 0;
      transform: translate(-50%, -50%) scale(0.5);
    }

    .ribbon-horizontal {
      width: 60px;
      height: 12px;
      background: linear-gradient(180deg, #c41e3a 0%, #8b1428 100%);
      position: relative;
      box-shadow: 0 2px 8px rgba(0,0,0,0.3);
    }

    .ribbon-vertical {
      width: 12px;
      height: 60px;
      background: linear-gradient(90deg, #c41e3a 0%, #8b1428 100%);
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      box-shadow: 0 2px 8px rgba(0,0,0,0.3);
    }

    .ribbon-bow {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 40px;
      height: 40px;
    }

    .bow-left, .bow-right {
      position: absolute;
      width: 20px;
      height: 30px;
      background: #c41e3a;
      border-radius: 50% 50% 50% 0;
      box-shadow: 0 2px 6px rgba(0,0,0,0.3);
    }

    .bow-left {
      left: -15px;
      top: 5px;
      transform: rotate(-45deg);
    }

    .bow-right {
      right: -15px;
      top: 5px;
      transform: rotate(135deg);
    }

    .bow-center {
      position: absolute;
      width: 12px;
      height: 12px;
      background: #8b1428;
      border-radius: 50%;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      box-shadow: 0 2px 4px rgba(0,0,0,0.4);
    }

    .stamps {
      position: absolute;
      top: 20px;
      right: 20px;
      display: flex;
      gap: 8px;
      z-index: 2;
    }

    .stamp {
      width: 50px;
      height: 60px;
      background: white;
      border: 3px solid #c41e3a;
      padding: 4px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.2);
      position: relative;
      animation: stampFloat 3s ease-in-out infinite;
    }

    .stamp:nth-child(2) {
      animation-delay: 1.5s;
    }

    @keyframes stampFloat {
      0%, 100% { transform: translateY(0px) rotate(0deg); }
      50% { transform: translateY(-5px) rotate(2deg); }
    }

    .stamp::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: repeating-linear-gradient(0deg, transparent, transparent 3px, #c41e3a 3px, #c41e3a 4px),
                  repeating-linear-gradient(90deg, transparent, transparent 3px, #c41e3a 3px, #c41e3a 4px);
      opacity: 0.3;
    }

    .stamp-image {
      width: 100%;
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 24px;
    }

    .postmark {
      position: absolute;
      top: 30px;
      right: 90px;
      width: 60px;
      height: 60px;
      border: 2px solid rgba(139, 20, 40, 0.4);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 10px;
      color: rgba(139, 20, 40, 0.6);
      transform: rotate(-15deg);
      z-index: 2;
    }

    .envelope-title {
      position: absolute;
      bottom: 30px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 18px;
      color: #5a4a3a;
      font-style: italic;
      z-index: 2;
      text-shadow: 1px 1px 2px rgba(255,255,255,0.8);
    }

    .gallery {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.5s ease;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      gap: 20px;
    }

    .gallery.active {
      opacity: 1;
      pointer-events: all;
    }

    .image-container {
      width: 500px;
      height: 600px;
      background: white;
      border: 8px solid #d4c5a9;
      box-shadow: 0 10px 40px rgba(0,0,0,0.3);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 48px;
      animation: slideIn 0.5s ease;
      position: relative;
    }

    .pages-container {
      display: flex;
      gap: 10px;
      margin-top: 15px;
      flex-wrap: wrap;
      justify-content: center;
      max-width: 600px;
    }

    .page-dot {
      width: 12px;
      height: 12px;
      border-radius: 50%;
      background: #ccc;
      cursor: pointer;
      transition: all 0.3s ease;
      position: relative;
    }

    .page-dot.active {
      background: #c41e3a;
      transform: scale(1.2);
    }

    .page-dot:hover {
      background: #8b1428;
      transform: scale(1.1);
    }

    .page-number {
      position: absolute;
      top: -25px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 10px;
      color: #666;
      opacity: 0;
      transition: opacity 0.3s ease;
    }

    .page-dot:hover .page-number {
      opacity: 1;
    }

    @keyframes slideIn {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .navigation {
      display: flex;
      gap: 20px;
      align-items: center;
    }

    .nav-button {
      padding: 12px 30px;
      background: #c41e3a;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 16px;
      font-family: 'Georgia', serif;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
      transition: all 0.3s ease;
    }

    .nav-button:hover {
      background: #8b1428;
      transform: translateY(-2px);
      box-shadow: 0 6px 16px rgba(0,0,0,0.3);
    }

    .nav-button:disabled {
      background: #ccc;
      cursor: not-allowed;
      transform: none;
    }

    .counter {
      font-size: 18px;
      color: #5a4a3a;
      font-weight: bold;
    }

    .close-button {
      position: absolute;
      top: 20px;
      right: 20px;
      width: 40px;
      height: 40px;
      background: #c41e3a;
      color: white;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      font-size: 24px;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
      transition: all 0.3s ease;
    }

    .close-button:hover {
      background: #8b1428;
      transform: rotate(90deg);
    }

    .empty-state {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      color: #666;
      font-size: 18px;
      text-align: center;
      gap: 10px;
    }

    .delete-button {
      position: absolute;
      top: 10px;
      right: 10px;
      width: 30px;
      height: 30px;
      background: rgba(196, 30, 58, 0.8);
      color: white;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      font-size: 16px;
      display: flex;
      align-items: center;
      justify-content: center;
      opacity: 1;
      transition: all 0.3s ease;
      z-index: 10;
    }

    .delete-button:hover {
      background: rgba(139, 20, 40, 0.9);
      transform: scale(1.1);
    }

    .confirm-delete {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background: rgba(255, 255, 255, 0.95);
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.3);
      text-align: center;
      z-index: 20;
      display: none;
    }

    .confirm-delete.show {
      display: block;
    }

    .confirm-buttons {
      display: flex;
      gap: 10px;
      margin-top: 15px;
      justify-content: center;
    }

    .confirm-btn {
      padding: 8px 16px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 14px;
      font-family: 'Georgia', serif;
      transition: all 0.3s ease;
    }

    .confirm-btn.yes {
      background: #dc3545;
      color: white;
    }

    .confirm-btn.yes:hover {
      background: #c82333;
    }

    .confirm-btn.no {
      background: #6c757d;
      color: white;
    }

    .confirm-btn.no:hover {
      background: #5a6268;
    }

    .loading {
      opacity: 0.5;
      pointer-events: none;
    }

    .toast {
      position: fixed;
      top: 20px;
      right: 20px;
      background: #c41e3a;
      color: white;
      padding: 15px 25px;
      border-radius: 8px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.3);
      z-index: 1000;
      opacity: 0;
      transform: translateX(100%);
      transition: all 0.3s ease;
    }

    .toast.show {
      opacity: 1;
      transform: translateX(0);
    }

    .toast.error {
      background: #dc3545;
    }

    .toast.success {
      background: #28a745;
    }

    .add-image-section {
      position: absolute;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
      display: flex;
      gap: 15px;
      align-items: center;
      background: rgba(255,255,255,0.9);
      padding: 15px 25px;
      border-radius: 8px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.2);
      flex-wrap: wrap;
      justify-content: center;
    }



    .add-button {
      padding: 10px 20px;
      background: #c41e3a;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 14px;
      font-family: 'Georgia', serif;
      transition: all 0.3s ease;
    }

    .add-button:hover {
      background: #8b1428;
    }

    .add-button:disabled {
      background: #ccc;
      cursor: not-allowed;
    }
  </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="https://cdn.tailwindcss.com" type="text/javascript"></script>
 </head>
 <body>
  <div class="container">
   <div class="sparkles">
    <div class="sparkle"></div>
    <div class="sparkle"></div>
    <div class="sparkle"></div>
    <div class="sparkle"></div>
    <div class="sparkle"></div>
    <div class="sparkle"></div>
    <div class="sparkle"></div>
    <div class="sparkle"></div>
    <div class="sparkle"></div>
    <div class="sparkle"></div>
    <div class="sparkle"></div>
    <div class="sparkle"></div>
    <div class="sparkle"></div>
    <div class="sparkle"></div>
    <div class="sparkle"></div>
   </div>
   <div class="envelope-wrapper" id="envelopeWrapper">
    <div class="envelope">
     <div class="envelope-texture"></div>
     <div class="envelope-flap"></div>
     <div class="ribbon">
      <div class="ribbon-horizontal"></div>
      <div class="ribbon-vertical"></div>
      <div class="ribbon-bow">
       <div class="bow-left"></div>
       <div class="bow-right"></div>
       <div class="bow-center"></div>
      </div>
     </div>
     <div class="stamps">
      <div class="stamp">
       <div class="stamp-image">
        🏛️
       </div>
      </div>
      <div class="stamp">
       <div class="stamp-image">
        📜
       </div>
      </div>
     </div>
     <div class="postmark"></div>
     <div class="envelope-title" id="envelopeTitle"></div>
    </div>
   </div>
   <div class="gallery" id="gallery"><button class="close-button" id="closeButton">×</button>
    <div class="image-container" id="imageContainer">
     <div class="empty-state">
      <div>
       📷
      </div>
      <div>
       Chưa có ảnh nào
      </div>
      <div style="font-size: 14px; color: #999;">
       Thiệp này chưa có ảnh kỷ niệm
      </div>
     </div>
    </div>
    <div class="navigation"><button class="nav-button" id="prevButton">← Trước</button>
     <div class="counter" id="counter">
      0 / 0
     </div><button class="nav-button" id="nextButton">Tiếp →</button>
    </div>
    <div class="pages-container" id="pagesContainer"></div><input type="file" class="file-input" id="fileInput" accept="image/*" multiple style="display: none;">
   </div>
  </div>
  <div class="toast" id="toast"></div>
  <script>
    const defaultConfig = {
      envelope_title: "Kỷ Niệm Đẹp",
      background_color: "#f5f5f0",
      envelope_color: "#f9f6f0",
      ribbon_color: "#c41e3a",
      text_color: "#5a4a3a",
      font_family: "Georgia"
    };

    let config = { ...defaultConfig };
    let currentImage = 1;
    let images = [];
    let isLoading = false;

    const envelopeWrapper = document.getElementById('envelopeWrapper');
    const gallery = document.getElementById('gallery');
    const imageContainer = document.getElementById('imageContainer');
    const counter = document.getElementById('counter');
    const prevButton = document.getElementById('prevButton');
    const nextButton = document.getElementById('nextButton');
    const closeButton = document.getElementById('closeButton');
    const fileInput = document.getElementById('fileInput');
    const toast = document.getElementById('toast');
    const pagesContainer = document.getElementById('pagesContainer');


    // Data handler for SDK
    const dataHandler = {
      onDataChanged(data) {
        images = data.sort((a, b) => new Date(a.createdAt) - new Date(b.createdAt));
        updateGalleryDisplay();
      }
    };

    // Initialize Data SDK
    async function initializeDataSdk() {
      if (window.dataSdk) {
        const result = await window.dataSdk.init(dataHandler);
        if (!result.isOk) {
          showToast('Lỗi khởi tạo dữ liệu', 'error');
        }
      }
    }

    envelopeWrapper.addEventListener('click', () => {
      envelopeWrapper.classList.add('opening');
      setTimeout(() => {
        envelopeWrapper.style.display = 'none';
        gallery.classList.add('active');
        updateGalleryDisplay();
      }, 1000);
    });

    prevButton.addEventListener('click', () => {
      if (currentImage > 1) {
        currentImage--;
        updateImageDisplay();
        updateCounter();
        updateNavigationButtons();
        updatePageDots();
      }
    });

    nextButton.addEventListener('click', () => {
      if (currentImage < images.length) {
        currentImage++;
        updateImageDisplay();
        updateCounter();
        updateNavigationButtons();
        updatePageDots();
      }
    });

    closeButton.addEventListener('click', () => {
      gallery.classList.remove('active');
      envelopeWrapper.style.display = 'block';
      envelopeWrapper.classList.remove('opening');
      currentImage = 1;
    });

    // Click on image container to add images
    imageContainer.addEventListener('click', (e) => {
      // Don't trigger if clicking on delete button
      if (e.target.classList.contains('delete-button')) {
        return;
      }
      fileInput.click();
    });

    fileInput.addEventListener('change', (event) => {
      console.log('File input changed:', event.target.files);
      handleFileSelect(event);
    });



    async function handleFileSelect(event) {
      const files = event.target.files;
      if (!files || files.length === 0) {
        showToast('Không có file nào được chọn', 'error');
        return;
      }

      if (images.length + files.length > 999) {
        showToast(`Chỉ có thể thêm ${999 - images.length} ảnh nữa`, 'error');
        return;
      }

      setLoading(true);
      let successCount = 0;

      try {
        for (let i = 0; i < files.length; i++) {
          const file = files[i];
          
          if (!file.type.startsWith('image/')) {
            showToast(`File ${file.name} không phải là ảnh`, 'error');
            continue;
          }

          try {
            const base64 = await fileToBase64(file);
            const imageData = {
              id: `img_${Date.now()}_${i}`,
              url: base64,
              name: file.name || `Ảnh ${images.length + i + 1}`,
              createdAt: new Date().toISOString()
            };

            if (window.dataSdk) {
              const result = await window.dataSdk.create(imageData);
              if (result.isOk) {
                successCount++;
              } else {
                console.error('SDK Error:', result.error);
                // Fallback: add to local array and update display
                images.push(imageData);
                successCount++;
                updateGalleryDisplay();
              }
            } else {
              // Fallback if SDK not available
              images.push(imageData);
              successCount++;
              updateGalleryDisplay();
            }
          } catch (fileError) {
            console.error('File processing error:', fileError);
            showToast(`Lỗi xử lý file ${file.name}: ${fileError.message}`, 'error');
          }
        }
      } catch (generalError) {
        console.error('General error:', generalError);
        showToast(`Lỗi chung: ${generalError.message}`, 'error');
      }

      fileInput.value = '';
      setLoading(false);
      
      if (successCount > 0) {
        showToast(`Đã thêm ${successCount} ảnh thành công!`, 'success');
        // Navigate to the first newly added image
        if (images.length > 0) {
          currentImage = Math.max(1, images.length - successCount + 1);
        }
        updateGalleryDisplay();
      } else {
        showToast('Không thể thêm ảnh nào', 'error');
      }
    }

    function fileToBase64(file) {
      return new Promise((resolve, reject) => {
        const reader = new FileReader();
        reader.onload = () => resolve(reader.result);
        reader.onerror = reject;
        reader.readAsDataURL(file);
      });
    }



    let imageToDelete = null;

    function showDeleteConfirmation(image) {
      imageToDelete = image;
      const confirmDialog = document.getElementById('confirmDialog');
      if (confirmDialog) {
        confirmDialog.classList.add('show');
      }
    }

    function cancelDelete() {
      imageToDelete = null;
      const confirmDialog = document.getElementById('confirmDialog');
      if (confirmDialog) {
        confirmDialog.classList.remove('show');
      }
    }

    async function confirmDeleteImage() {
      if (!imageToDelete) return;
      
      const confirmDialog = document.getElementById('confirmDialog');
      if (confirmDialog) {
        confirmDialog.classList.remove('show');
      }

      setLoading(true);

      if (window.dataSdk) {
        const result = await window.dataSdk.delete(imageToDelete);
        if (result.isOk) {
          showToast('Đã xóa ảnh thành công!', 'success');
          // Adjust currentImage after deletion
          const deletedIndex = images.findIndex(img => img.id === imageToDelete.id);
          if (deletedIndex !== -1 && deletedIndex < currentImage - 1) {
            currentImage--;
          } else if (currentImage > images.length - 1 && currentImage > 1) {
            currentImage--;
          }
        } else {
          showToast('Lỗi khi xóa ảnh', 'error');
        }
      } else {
        // Fallback: remove from local array
        const index = images.findIndex(img => img.id === imageToDelete.id);
        if (index !== -1) {
          images.splice(index, 1);
          showToast('Đã xóa ảnh thành công!', 'success');
          if (currentImage > images.length && currentImage > 1) {
            currentImage--;
          }
          updateGalleryDisplay();
        }
      }

      imageToDelete = null;
      setLoading(false);
    }

    function updateGalleryDisplay() {
      if (images.length === 0) {
        currentImage = 1;
        showEmptyState();
      } else {
        // Ensure currentImage is within valid range
        if (currentImage > images.length) {
          currentImage = images.length;
        }
        if (currentImage < 1) {
          currentImage = 1;
        }
        updateImageDisplay();
      }
      updateCounter();
      updateNavigationButtons();
      updatePageDots();
    }

    function updatePageDots() {
      pagesContainer.innerHTML = '';
      
      if (images.length === 0) {
        return;
      }

      for (let i = 1; i <= images.length; i++) {
        const dot = document.createElement('div');
        dot.className = `page-dot ${i === currentImage ? 'active' : ''}`;
        
        const pageNumber = document.createElement('div');
        pageNumber.className = 'page-number';
        pageNumber.textContent = i;
        dot.appendChild(pageNumber);
        
        dot.addEventListener('click', () => {
          currentImage = i;
          updateImageDisplay();
          updateCounter();
          updateNavigationButtons();
          updatePageDots();
        });
        
        pagesContainer.appendChild(dot);
      }
    }

    function updateImageDisplay() {
      if (images.length === 0) {
        showEmptyState();
        return;
      }

      const image = images[currentImage - 1];
      const img = document.createElement('img');
      img.src = image.url;
      img.alt = image.name;
      img.style.cssText = 'width: 100%; height: 100%; object-fit: cover; border-radius: 4px;';
      
      img.onerror = function() {
        this.style.display = 'none';
        const errorDiv = document.createElement('div');
        errorDiv.style.cssText = 'display: flex; align-items: center; justify-content: center; font-size: 18px; color: #999; flex-direction: column; gap: 10px;';
        errorDiv.innerHTML = '<div>❌</div><div>Không thể tải ảnh</div>';
        imageContainer.appendChild(errorDiv);
      };

      const deleteBtn = document.createElement('button');
      deleteBtn.className = 'delete-button';
      deleteBtn.innerHTML = '×';
      deleteBtn.onclick = (e) => {
        e.stopPropagation();
        showDeleteConfirmation(image);
      };

      const confirmDialog = document.createElement('div');
      confirmDialog.className = 'confirm-delete';
      confirmDialog.id = 'confirmDialog';
      confirmDialog.innerHTML = `
        <div style="font-size: 16px; color: #333; margin-bottom: 10px;">Bạn có chắc muốn xóa ảnh này?</div>
        <div style="font-size: 14px; color: #666;">${image.name}</div>
        <div class="confirm-buttons">
          <button class="confirm-btn yes" onclick="confirmDeleteImage()">Xóa</button>
          <button class="confirm-btn no" onclick="cancelDelete()">Hủy</button>
        </div>
      `;
      
      imageContainer.innerHTML = '';
      imageContainer.appendChild(img);
      imageContainer.appendChild(deleteBtn);
      imageContainer.appendChild(confirmDialog);
      
      imageContainer.style.animation = 'none';
      setTimeout(() => {
        imageContainer.style.animation = 'slideIn 0.5s ease';
      }, 10);
    }

    function showEmptyState() {
      imageContainer.innerHTML = `
        <div class="empty-state">
          <div>📷</div>
          <div>Chưa có ảnh nào</div>
          <div style="font-size: 14px; color: #999;">Nhấn vào đây để thêm ảnh</div>
        </div>
      `;
    }

    function updateCounter() {
      counter.textContent = `${images.length > 0 ? currentImage : 0} / ${images.length}`;
    }

    function updateNavigationButtons() {
      prevButton.disabled = currentImage <= 1 || images.length === 0;
      nextButton.disabled = currentImage >= images.length || images.length === 0;
    }

    function setLoading(loading) {
      isLoading = loading;
      
      if (loading) {
        gallery.classList.add('loading');
      } else {
        gallery.classList.remove('loading');
      }
    }

    function showToast(message, type = 'info') {
      toast.textContent = message;
      toast.className = `toast ${type} show`;
      
      setTimeout(() => {
        toast.classList.remove('show');
      }, 3000);
    }

    async function onConfigChange(newConfig) {
      const titleElement = document.getElementById('envelopeTitle');
      if (titleElement) {
        titleElement.textContent = newConfig.envelope_title || defaultConfig.envelope_title;
      }
      
      document.body.style.background = newConfig.background_color || defaultConfig.background_color;
      
      const envelopeElements = document.querySelectorAll('.envelope, .envelope-flap');
      envelopeElements.forEach(el => {
        el.style.background = newConfig.envelope_color || defaultConfig.envelope_color;
      });
      
      const ribbonElements = document.querySelectorAll('.ribbon-horizontal, .ribbon-vertical, .bow-left, .bow-right');
      ribbonElements.forEach(el => {
        el.style.background = newConfig.ribbon_color || defaultConfig.ribbon_color;
      });
      
      const textElements = document.querySelectorAll('.envelope-title, .counter');
      textElements.forEach(el => {
        el.style.color = newConfig.text_color || defaultConfig.text_color;
      });
      
      const customFont = newConfig.font_family || defaultConfig.font_family;
      document.body.style.fontFamily = `${customFont}, serif`;
    }

    // Initialize
    onConfigChange(config);
    initializeDataSdk();

    if (window.elementSdk) {
      window.elementSdk.init({
        defaultConfig,
        onConfigChange,
        mapToCapabilities: (config) => ({
          recolorables: [
            {
              get: () => config.background_color || defaultConfig.background_color,
              set: (value) => {
                config.background_color = value;
                window.elementSdk.setConfig({ background_color: value });
              }
            },
            {
              get: () => config.envelope_color || defaultConfig.envelope_color,
              set: (value) => {
                config.envelope_color = value;
                window.elementSdk.setConfig({ envelope_color: value });
              }
            },
            {
              get: () => config.ribbon_color || defaultConfig.ribbon_color,
              set: (value) => {
                config.ribbon_color = value;
                window.elementSdk.setConfig({ ribbon_color: value });
              }
            },
            {
              get: () => config.text_color || defaultConfig.text_color,
              set: (value) => {
                config.text_color = value;
                window.elementSdk.setConfig({ text_color: value });
              }
            }
          ],
          borderables: [],
          fontEditable: {
            get: () => config.font_family || defaultConfig.font_family,
            set: (value) => {
              config.font_family = value;
              window.elementSdk.setConfig({ font_family: value });
            }
          },
          fontSizeable: undefined
        }),
        mapToEditPanelValues: (config) => new Map([
          ["envelope_title", config.envelope_title || defaultConfig.envelope_title]
        ])
      });
    }
  </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9999a79894b16bb2',t:'MTc2MjMxNzQzNC4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
