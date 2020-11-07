---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: b01f8d356d83cb111441cf911750056033422fe8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911384"
---
# <span data-ttu-id="89dd9-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="89dd9-101">Save-AzVMImage</span></span>

## <span data-ttu-id="89dd9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="89dd9-103">Сохранение виртуальной машины в виде VMImage.</span><span class="sxs-lookup"><span data-stu-id="89dd9-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="89dd9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89dd9-104">SYNTAX</span></span>

### <span data-ttu-id="89dd9-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89dd9-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89dd9-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="89dd9-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89dd9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89dd9-107">DESCRIPTION</span></span>
<span data-ttu-id="89dd9-108">Командлет **Save-AzVMImage** сохраняет виртуальную машину как VMImage.</span><span class="sxs-lookup"><span data-stu-id="89dd9-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="89dd9-109">Перед созданием образа виртуальной машины выполните команду Sysprep для виртуальной машины, а затем пометьте ее как обобщенную с помощью командлета Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="89dd9-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>

<span data-ttu-id="89dd9-110">Результатом этого командлета является шаблон JSON (объектная нотация).</span><span class="sxs-lookup"><span data-stu-id="89dd9-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="89dd9-111">Вы можете развернуть виртуальные машины из записанного образа.</span><span class="sxs-lookup"><span data-stu-id="89dd9-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="89dd9-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89dd9-112">EXAMPLES</span></span>

### <span data-ttu-id="89dd9-113">Пример 1: запись виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="89dd9-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="89dd9-114">Первая команда помечает виртуальную машину с именем VirtualMachine07 как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="89dd9-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="89dd9-115">Вторая команда перехватывает виртуальную машину с именем VirtualMachine07 как VMImage.</span><span class="sxs-lookup"><span data-stu-id="89dd9-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="89dd9-116">Свойство **Output** ВОЗВРАЩАЕТ шаблон JSON.</span><span class="sxs-lookup"><span data-stu-id="89dd9-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="89dd9-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89dd9-117">PARAMETERS</span></span>

### <span data-ttu-id="89dd9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89dd9-118">-AsJob</span></span>
<span data-ttu-id="89dd9-119">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="89dd9-119">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dd9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89dd9-120">-DefaultProfile</span></span>
<span data-ttu-id="89dd9-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89dd9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89dd9-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="89dd9-122">-DestinationContainerName</span></span>
<span data-ttu-id="89dd9-123">Указывает имя контейнера в контейнере System, который вы хотите хранить для изображений.</span><span class="sxs-lookup"><span data-stu-id="89dd9-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="89dd9-124">Если контейнер не существует, он создается для вас.</span><span class="sxs-lookup"><span data-stu-id="89dd9-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="89dd9-125">Виртуальные жесткие диски (VHD), составляющие VMImage, находятся в контейнере, указанном в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="89dd9-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="89dd9-126">Если виртуальные жесткие диски распределены между несколькими учетными записями хранения, этот командлет создает один контейнер с этим именем в каждой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="89dd9-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="89dd9-127">URL-адрес сохраненного изображения подобен:</span><span class="sxs-lookup"><span data-stu-id="89dd9-127">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="89dd9-128"> HTTPS:// \< storageAccountName \> . BLOB.Core.Windows.NET/System/Microsoft.COMPUTE/Images/ \< imagesContainer \> / \< vhdPrefix-osDisk \> . XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX. VHD.</span><span class="sxs-lookup"><span data-stu-id="89dd9-128">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="89dd9-129">-ID</span><span class="sxs-lookup"><span data-stu-id="89dd9-129">-Id</span></span>
<span data-ttu-id="89dd9-130">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="89dd9-130">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="89dd9-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="89dd9-131">-Name</span></span>
<span data-ttu-id="89dd9-132">Задает имя.</span><span class="sxs-lookup"><span data-stu-id="89dd9-132">Specifies a name.</span></span>

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

### <span data-ttu-id="89dd9-133">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="89dd9-133">-Overwrite</span></span>
<span data-ttu-id="89dd9-134">Указывает на то, что этот командлет перезаписывает все виртуальные жесткие диски с таким же префиксом в конечном контейнере.</span><span class="sxs-lookup"><span data-stu-id="89dd9-134">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="89dd9-135">-Path</span><span class="sxs-lookup"><span data-stu-id="89dd9-135">-Path</span></span>
<span data-ttu-id="89dd9-136">Указывает путь к виртуальному жесткому диску.</span><span class="sxs-lookup"><span data-stu-id="89dd9-136">Specifies the path of the VHD.</span></span>

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

### <span data-ttu-id="89dd9-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89dd9-137">-ResourceGroupName</span></span>
<span data-ttu-id="89dd9-138">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="89dd9-138">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="89dd9-139">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="89dd9-139">-VHDNamePrefix</span></span>
<span data-ttu-id="89dd9-140">Указывает префикс в имени больших двоичных объектов, составляющих профиль хранилища для VMImage.</span><span class="sxs-lookup"><span data-stu-id="89dd9-140">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="89dd9-141">Например, префикс vhdPrefix для диска операционной системы приводит к имени vhdPrefix-osdisk. \< GUID \> . VHD.</span><span class="sxs-lookup"><span data-stu-id="89dd9-141">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="89dd9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89dd9-142">CommonParameters</span></span>
<span data-ttu-id="89dd9-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89dd9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89dd9-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89dd9-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89dd9-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89dd9-145">INPUTS</span></span>

### <span data-ttu-id="89dd9-146">Ничего</span><span class="sxs-lookup"><span data-stu-id="89dd9-146">None</span></span>
<span data-ttu-id="89dd9-147">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="89dd9-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="89dd9-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89dd9-148">OUTPUTS</span></span>

### <span data-ttu-id="89dd9-149">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="89dd9-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="89dd9-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="89dd9-150">NOTES</span></span>

## <span data-ttu-id="89dd9-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89dd9-151">RELATED LINKS</span></span>

[<span data-ttu-id="89dd9-152">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="89dd9-152">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="89dd9-153">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="89dd9-153">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="89dd9-154">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="89dd9-154">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="89dd9-155">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="89dd9-155">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="89dd9-156">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="89dd9-156">Set-AzVM</span></span>](./Set-AzVM.md)


