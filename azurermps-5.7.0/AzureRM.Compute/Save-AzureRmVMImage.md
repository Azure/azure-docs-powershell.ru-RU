---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: 8f3aebe1e9e79423d7251fa79084d6fa85407b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568620"
---
# <span data-ttu-id="5726c-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="5726c-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="5726c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5726c-102">SYNOPSIS</span></span>
<span data-ttu-id="5726c-103">Сохранение виртуальной машины в виде VMImage.</span><span class="sxs-lookup"><span data-stu-id="5726c-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5726c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5726c-104">SYNTAX</span></span>

### <span data-ttu-id="5726c-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5726c-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [<CommonParameters>]
```

### <span data-ttu-id="5726c-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="5726c-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [<CommonParameters>]
```

## <span data-ttu-id="5726c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5726c-107">DESCRIPTION</span></span>
<span data-ttu-id="5726c-108">Командлет **Save-AzureRmVMImage** сохраняет виртуальную машину как VMImage.</span><span class="sxs-lookup"><span data-stu-id="5726c-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="5726c-109">Перед созданием образа виртуальной машины выполните команду Sysprep для виртуальной машины, а затем пометьте ее как обобщенную с помощью командлета Set-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="5726c-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="5726c-110">Результатом этого командлета является шаблон JSON (объектная нотация).</span><span class="sxs-lookup"><span data-stu-id="5726c-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="5726c-111">Вы можете развернуть виртуальные машины из записанного образа.</span><span class="sxs-lookup"><span data-stu-id="5726c-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="5726c-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5726c-112">EXAMPLES</span></span>

### <span data-ttu-id="5726c-113">Пример 1: запись виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="5726c-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="5726c-114">Первая команда помечает виртуальную машину с именем VirtualMachine07 как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="5726c-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="5726c-115">Вторая команда перехватывает виртуальную машину с именем VirtualMachine07 как VMImage.</span><span class="sxs-lookup"><span data-stu-id="5726c-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="5726c-116">Свойство **Output** ВОЗВРАЩАЕТ шаблон JSON.</span><span class="sxs-lookup"><span data-stu-id="5726c-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="5726c-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5726c-117">PARAMETERS</span></span>

### <span data-ttu-id="5726c-118">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="5726c-118">-DestinationContainerName</span></span>
<span data-ttu-id="5726c-119">Указывает имя контейнера в контейнере System, который вы хотите хранить для изображений.</span><span class="sxs-lookup"><span data-stu-id="5726c-119">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="5726c-120">Если контейнер не существует, он создается для вас.</span><span class="sxs-lookup"><span data-stu-id="5726c-120">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="5726c-121">Виртуальные жесткие диски (VHD), составляющие VMImage, находятся в контейнере, указанном в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="5726c-121">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="5726c-122">Если виртуальные жесткие диски распределены между несколькими учетными записями хранения, этот командлет создает один контейнер с этим именем в каждой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="5726c-122">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="5726c-123">URL-адрес сохраненного изображения подобен:</span><span class="sxs-lookup"><span data-stu-id="5726c-123">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="5726c-124"> HTTPS:// \<storageAccountName\> . BLOB.Core.Windows.NET/System/Microsoft.COMPUTE/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX. VHD.</span><span class="sxs-lookup"><span data-stu-id="5726c-124">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5726c-125">-ID</span><span class="sxs-lookup"><span data-stu-id="5726c-125">-Id</span></span>
<span data-ttu-id="5726c-126">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5726c-126">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5726c-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5726c-127">-Name</span></span>
<span data-ttu-id="5726c-128">Задает имя.</span><span class="sxs-lookup"><span data-stu-id="5726c-128">Specifies a name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5726c-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="5726c-129">-Overwrite</span></span>
<span data-ttu-id="5726c-130">Указывает на то, что этот командлет перезаписывает все виртуальные жесткие диски с таким же префиксом в конечном контейнере.</span><span class="sxs-lookup"><span data-stu-id="5726c-130">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5726c-131">-Path</span><span class="sxs-lookup"><span data-stu-id="5726c-131">-Path</span></span>
<span data-ttu-id="5726c-132">Указывает путь к виртуальному жесткому диску.</span><span class="sxs-lookup"><span data-stu-id="5726c-132">Specifies the path of the VHD.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5726c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5726c-133">-ResourceGroupName</span></span>
<span data-ttu-id="5726c-134">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5726c-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5726c-135">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="5726c-135">-VHDNamePrefix</span></span>
<span data-ttu-id="5726c-136">Указывает префикс в имени больших двоичных объектов, составляющих профиль хранилища для VMImage.</span><span class="sxs-lookup"><span data-stu-id="5726c-136">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="5726c-137">Например, префикс vhdPrefix для диска операционной системы приводит к присвоению имени vhdPrefix-osdisk. \<guid\> . VHD.</span><span class="sxs-lookup"><span data-stu-id="5726c-137">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5726c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5726c-138">CommonParameters</span></span>
<span data-ttu-id="5726c-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5726c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5726c-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5726c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5726c-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5726c-141">INPUTS</span></span>

### <span data-ttu-id="5726c-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="5726c-142">None</span></span>
<span data-ttu-id="5726c-143">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5726c-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5726c-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5726c-144">OUTPUTS</span></span>

## <span data-ttu-id="5726c-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="5726c-145">NOTES</span></span>

## <span data-ttu-id="5726c-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5726c-146">RELATED LINKS</span></span>

[<span data-ttu-id="5726c-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="5726c-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="5726c-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="5726c-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="5726c-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="5726c-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="5726c-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="5726c-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="5726c-151">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5726c-151">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


