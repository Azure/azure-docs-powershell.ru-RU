---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: b6d8d21eea863683912e204403ebe5a75ac40fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556768"
---
# <span data-ttu-id="f030f-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f030f-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="f030f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f030f-102">SYNOPSIS</span></span>
<span data-ttu-id="f030f-103">Сохранение виртуальной машины в виде VMImage.</span><span class="sxs-lookup"><span data-stu-id="f030f-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f030f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f030f-104">SYNTAX</span></span>

### <span data-ttu-id="f030f-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f030f-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f030f-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f030f-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f030f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f030f-107">DESCRIPTION</span></span>
<span data-ttu-id="f030f-108">Командлет **Save-AzureRmVMImage** сохраняет виртуальную машину как VMImage.</span><span class="sxs-lookup"><span data-stu-id="f030f-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="f030f-109">Перед созданием образа виртуальной машины выполните команду Sysprep для виртуальной машины, а затем пометьте ее как обобщенную с помощью командлета Set-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="f030f-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="f030f-110">Результатом этого командлета является шаблон JSON (объектная нотация).</span><span class="sxs-lookup"><span data-stu-id="f030f-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="f030f-111">Вы можете развернуть виртуальные машины из записанного образа.</span><span class="sxs-lookup"><span data-stu-id="f030f-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="f030f-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f030f-112">EXAMPLES</span></span>

### <span data-ttu-id="f030f-113">Пример 1: запись виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="f030f-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="f030f-114">Первая команда помечает виртуальную машину с именем VirtualMachine07 как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="f030f-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="f030f-115">Вторая команда перехватывает виртуальную машину с именем VirtualMachine07 как VMImage.</span><span class="sxs-lookup"><span data-stu-id="f030f-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="f030f-116">Свойство **Output** ВОЗВРАЩАЕТ шаблон JSON.</span><span class="sxs-lookup"><span data-stu-id="f030f-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="f030f-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f030f-117">PARAMETERS</span></span>

### <span data-ttu-id="f030f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f030f-118">-AsJob</span></span>
<span data-ttu-id="f030f-119">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f030f-119">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f030f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f030f-120">-DefaultProfile</span></span>
<span data-ttu-id="f030f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f030f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f030f-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="f030f-122">-DestinationContainerName</span></span>
<span data-ttu-id="f030f-123">Указывает имя контейнера в контейнере System, который вы хотите хранить для изображений.</span><span class="sxs-lookup"><span data-stu-id="f030f-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="f030f-124">Если контейнер не существует, он создается для вас.</span><span class="sxs-lookup"><span data-stu-id="f030f-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="f030f-125">Виртуальные жесткие диски (VHD), составляющие VMImage, находятся в контейнере, указанном в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="f030f-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="f030f-126">Если виртуальные жесткие диски распределены между несколькими учетными записями хранения, этот командлет создает один контейнер с этим именем в каждой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f030f-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="f030f-127">URL-адрес сохраненного изображения подобен: https:// \<storageAccountName\> . BLOB.Core.Windows.NET/System/Microsoft.COMPUTE/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX. VHD.</span><span class="sxs-lookup"><span data-stu-id="f030f-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f030f-128">-ID</span><span class="sxs-lookup"><span data-stu-id="f030f-128">-Id</span></span>
<span data-ttu-id="f030f-129">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f030f-129">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f030f-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f030f-130">-Name</span></span>
<span data-ttu-id="f030f-131">Задает имя.</span><span class="sxs-lookup"><span data-stu-id="f030f-131">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f030f-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f030f-132">-Overwrite</span></span>
<span data-ttu-id="f030f-133">Указывает на то, что этот командлет перезаписывает все виртуальные жесткие диски с таким же префиксом в конечном контейнере.</span><span class="sxs-lookup"><span data-stu-id="f030f-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f030f-134">-Path</span><span class="sxs-lookup"><span data-stu-id="f030f-134">-Path</span></span>
<span data-ttu-id="f030f-135">Путь к файлу, в котором хранится шаблон записанного изображения.</span><span class="sxs-lookup"><span data-stu-id="f030f-135">The file path in which the template of the captured image is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f030f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f030f-136">-ResourceGroupName</span></span>
<span data-ttu-id="f030f-137">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f030f-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f030f-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="f030f-138">-VHDNamePrefix</span></span>
<span data-ttu-id="f030f-139">Указывает префикс в имени больших двоичных объектов, составляющих профиль хранилища для VMImage.</span><span class="sxs-lookup"><span data-stu-id="f030f-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="f030f-140">Например, префикс vhdPrefix для диска операционной системы приводит к присвоению имени vhdPrefix-osdisk. \<guid\> . VHD.</span><span class="sxs-lookup"><span data-stu-id="f030f-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f030f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f030f-141">CommonParameters</span></span>
<span data-ttu-id="f030f-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f030f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f030f-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f030f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f030f-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f030f-144">INPUTS</span></span>

### <span data-ttu-id="f030f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f030f-145">System.String</span></span>

### <span data-ttu-id="f030f-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f030f-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f030f-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f030f-147">OUTPUTS</span></span>

### <span data-ttu-id="f030f-148">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="f030f-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="f030f-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="f030f-149">NOTES</span></span>

## <span data-ttu-id="f030f-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f030f-150">RELATED LINKS</span></span>

[<span data-ttu-id="f030f-151">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f030f-151">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="f030f-152">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f030f-152">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="f030f-153">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f030f-153">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="f030f-154">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f030f-154">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="f030f-155">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f030f-155">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


