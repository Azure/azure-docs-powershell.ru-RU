---
title: Использование Azure PowerShell в Docker
description: Использование предустановки Azure PowerShell в образе Docker.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.openlocfilehash: b5ad201abcabbdc1a88db241b028d88f05054a14
ms.sourcegitcommit: cef87acc9f2a0d296bef74f526afd2e067e8146b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/02/2020
ms.locfileid: "84299457"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="2e35f-103">Использование Azure PowerShell в Docker</span><span class="sxs-lookup"><span data-stu-id="2e35f-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="2e35f-104">Мы публикуем образы Docker с предустановкой Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2e35f-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="2e35f-105">В этой статье показано, как приступить к работе с Azure PowerShell в контейнере Docker.</span><span class="sxs-lookup"><span data-stu-id="2e35f-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="2e35f-106">Поиск доступных образов</span><span class="sxs-lookup"><span data-stu-id="2e35f-106">Finding available images</span></span>

<span data-ttu-id="2e35f-107">Для выпущенных образов требуется Docker 17.05 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="2e35f-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="2e35f-108">Также предполагается, что Docker можно запускать без `sudo` или прав локального администратора.</span><span class="sxs-lookup"><span data-stu-id="2e35f-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="2e35f-109">Чтобы правильно установить `docker`, следуйте официальным [инструкциям][install] Docker.</span><span class="sxs-lookup"><span data-stu-id="2e35f-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="2e35f-110">Последняя версия образа контейнера содержит последнюю версию PowerShell и последние версии модулей Azure PowerShell, поддерживаемые модулем Az.</span><span class="sxs-lookup"><span data-stu-id="2e35f-110">The latest container image contains the latest version of PowerShell and the latest Azure PowerShell modules supported with the Az module.</span></span>

<span data-ttu-id="2e35f-111">Вместе с каждым новым выпуском модуля Az мы выпускаем образ для приведенных ниже операционных систем.</span><span class="sxs-lookup"><span data-stu-id="2e35f-111">For each new release of the Az module we are releasing an image for the following operating systems:</span></span>

- <span data-ttu-id="2e35f-112">Ubuntu 18.04 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2e35f-112">Ubuntu 18.04 (default)</span></span>
- <span data-ttu-id="2e35f-113">Debian 9</span><span class="sxs-lookup"><span data-stu-id="2e35f-113">Debian 9</span></span>
- <span data-ttu-id="2e35f-114">CentOS 7</span><span class="sxs-lookup"><span data-stu-id="2e35f-114">CentOs 7</span></span>

<span data-ttu-id="2e35f-115">См. [полный список доступных образов Docker][az image].</span><span class="sxs-lookup"><span data-stu-id="2e35f-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="2e35f-116">Использование Azure PowerShell в контейнере</span><span class="sxs-lookup"><span data-stu-id="2e35f-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="2e35f-117">Ниже представлены команды Docker, необходимые для скачивания образа и запуска интерактивного сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2e35f-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="2e35f-118">Скачайте последнюю версию образа azure-powershell.</span><span class="sxs-lookup"><span data-stu-id="2e35f-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="2e35f-119">Запустите контейнер azure-powershell в интерактивном режиме:</span><span class="sxs-lookup"><span data-stu-id="2e35f-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

<span data-ttu-id="2e35f-120">Для узлов Windows Docker нужно включить общий доступ к файлам Docker, чтобы предоставить контейнерам Linux общий доступ к локальным диски в Windows.</span><span class="sxs-lookup"><span data-stu-id="2e35f-120">For Windows Docker hosts, you must enable Docker File Sharing to allow local drives on Windows to be shared with Linux containers.</span></span> <span data-ttu-id="2e35f-121">Дополнительные сведения см. в статье [Начало работы с Docker для Windows][file-sharing].</span><span class="sxs-lookup"><span data-stu-id="2e35f-121">For more information see [Get started with Docker for Windows][file-sharing].</span></span>

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="2e35f-122">Запуск контейнера azure-powershell в интерактивном режиме с использованием проверки подлинности узла</span><span class="sxs-lookup"><span data-stu-id="2e35f-122">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="2e35f-123">Если в системе с Docker есть установка Azure PowerShell, возможно, доступны кэшированные учетные данные Azure.</span><span class="sxs-lookup"><span data-stu-id="2e35f-123">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="2e35f-124">Эти учетные данные можно использовать в сеансе PowerShell, выполняющемся в контейнере Docker.</span><span class="sxs-lookup"><span data-stu-id="2e35f-124">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="2e35f-125">По умолчанию кэшированные учетные данные находятся в каталоге `$HOME/.Azure` на узле.</span><span class="sxs-lookup"><span data-stu-id="2e35f-125">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="2e35f-126">Служба Docker должна иметь доступ к этому расположению для получения доступа к учетным данным.</span><span class="sxs-lookup"><span data-stu-id="2e35f-126">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="2e35f-127">Следующая команда запускает контейнер с подключенным кэшем учетных данных, а также интерактивный сеанс PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2e35f-127">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="2e35f-128">Удаление ненужного образа</span><span class="sxs-lookup"><span data-stu-id="2e35f-128">Remove the image when no longer needed</span></span>

<span data-ttu-id="2e35f-129">Приведенная ниже команда служит для удаления контейнера Docker, если он больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="2e35f-129">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="2e35f-130">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="2e35f-130">Next steps</span></span>

<span data-ttu-id="2e35f-131">Дополнительные сведения о модулях Azure PowerShell и их функциях см. в статье [Get Started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="2e35f-131">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
