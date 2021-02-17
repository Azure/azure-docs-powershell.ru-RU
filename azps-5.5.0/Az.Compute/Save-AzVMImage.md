---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: 0d2a4ade662ec23a4a139460bce8fe5387683120
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238733"
---
# <span data-ttu-id="ed2bc-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ed2bc-101">Save-AzVMImage</span></span>

## <span data-ttu-id="ed2bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ed2bc-103">Сохраняет виртуальную машину в качестве VMImage.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="ed2bc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ed2bc-104">SYNTAX</span></span>

### <span data-ttu-id="ed2bc-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed2bc-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed2bc-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ed2bc-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed2bc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed2bc-107">DESCRIPTION</span></span>
<span data-ttu-id="ed2bc-108">При **этом** виртуальная машинка сохраняется как VMImage.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="ed2bc-109">Прежде чем создавать изображение виртуальной машины, с помощью Set-AzVM пометить ее как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="ed2bc-110">Результат этого cmdlet — шаблон нотации объектов JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="ed2bc-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="ed2bc-111">Вы можете развернуть виртуальные машины из захваченного изображения.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="ed2bc-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ed2bc-112">EXAMPLES</span></span>

### <span data-ttu-id="ed2bc-113">Пример 1. Захват виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="ed2bc-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="ed2bc-114">Первая команда пометит виртуальную машину с именем VirtualMachine07 как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="ed2bc-115">Вторая команда фиксирует виртуальную машину с именем VirtualMachine07 в качестве VMImage.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="ed2bc-116">Свойство **Output** возвращает шаблон JSON.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="ed2bc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed2bc-117">PARAMETERS</span></span>

### <span data-ttu-id="ed2bc-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed2bc-118">-AsJob</span></span>
<span data-ttu-id="ed2bc-119">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ed2bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed2bc-120">-DefaultProfile</span></span>
<span data-ttu-id="ed2bc-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed2bc-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="ed2bc-122">-DestinationContainerName</span></span>
<span data-ttu-id="ed2bc-123">Указывает имя контейнера внутри "системного" контейнера, который нужно удерживать на своих изображениях.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="ed2bc-124">Если контейнера нет, он создается для вас.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="ed2bc-125">Виртуальные жесткие диски (VHD), которые образуют VMImage, находятся в контейнере, который определяет этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="ed2bc-126">Если VHD-коды распределяются по нескольким учетным записям, с его учетной записью создается один контейнер с этим именем.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="ed2bc-127">URL-адрес сохраненного изображения аналогилен https:// \<storageAccountName\> .blob.core.windows.net/system/Microsoft.Compute/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> .xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxx.vhd.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="ed2bc-128">-Id</span><span class="sxs-lookup"><span data-stu-id="ed2bc-128">-Id</span></span>
<span data-ttu-id="ed2bc-129">Определяет ИД ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-129">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="ed2bc-130">-Name</span><span class="sxs-lookup"><span data-stu-id="ed2bc-130">-Name</span></span>
<span data-ttu-id="ed2bc-131">Указывает имя.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-131">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed2bc-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="ed2bc-132">-Overwrite</span></span>
<span data-ttu-id="ed2bc-133">Указывает на то, что этот cmdlet перезаписает все VHD-коды с одинаковым префиксом в контейнере назначения.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="ed2bc-134">-Path</span><span class="sxs-lookup"><span data-stu-id="ed2bc-134">-Path</span></span>
<span data-ttu-id="ed2bc-135">Путь к файлу, в котором хранится шаблон рисунка.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-135">The file path in which the template of the captured image is stored.</span></span>

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

### <span data-ttu-id="ed2bc-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed2bc-136">-ResourceGroupName</span></span>
<span data-ttu-id="ed2bc-137">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ed2bc-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="ed2bc-138">-VHDNamePrefix</span></span>
<span data-ttu-id="ed2bc-139">Указывает префикс в именах BLOB-имен, которые образуют профиль хранилища VMImage.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="ed2bc-140">Например, префикс vhdPrefix для диска операционной системы приводит к имени vhdPrefix-osdisk. \<guid\> vhd.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="ed2bc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed2bc-141">CommonParameters</span></span>
<span data-ttu-id="ed2bc-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed2bc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed2bc-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed2bc-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed2bc-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed2bc-144">INPUTS</span></span>

### <span data-ttu-id="ed2bc-145">System.String</span><span class="sxs-lookup"><span data-stu-id="ed2bc-145">System.String</span></span>

### <span data-ttu-id="ed2bc-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ed2bc-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ed2bc-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ed2bc-147">OUTPUTS</span></span>

### <span data-ttu-id="ed2bc-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="ed2bc-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="ed2bc-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ed2bc-149">NOTES</span></span>

## <span data-ttu-id="ed2bc-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed2bc-150">RELATED LINKS</span></span>

[<span data-ttu-id="ed2bc-151">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ed2bc-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="ed2bc-152">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="ed2bc-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="ed2bc-153">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="ed2bc-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="ed2bc-154">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="ed2bc-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="ed2bc-155">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="ed2bc-155">Set-AzVM</span></span>](./Set-AzVM.md)


