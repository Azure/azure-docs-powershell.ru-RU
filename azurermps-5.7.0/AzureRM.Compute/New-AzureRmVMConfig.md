---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 45cb93e652f9c1524ef1bb11972f184336ef7328
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732752"
---
# <span data-ttu-id="bfec5-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="bfec5-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="bfec5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bfec5-102">SYNOPSIS</span></span>
<span data-ttu-id="bfec5-103">Создание настраиваемого объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bfec5-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfec5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bfec5-104">SYNTAX</span></span>

```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [-LicenseType <String>] [-IdentityType <ResourceIdentityType>] [-Tags <Hashtable>] [<CommonParameters>]
```

## <span data-ttu-id="bfec5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfec5-105">DESCRIPTION</span></span>
<span data-ttu-id="bfec5-106">Командлет **New-AzureRmVMConfig** создает настраиваемый локальный объект виртуальной машины для Azure.</span><span class="sxs-lookup"><span data-stu-id="bfec5-106">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="bfec5-107">Другие командлеты можно использовать для настройки объекта виртуальной машины, например Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface и Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="bfec5-107">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="bfec5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bfec5-108">EXAMPLES</span></span>

### <span data-ttu-id="bfec5-109">Пример 1: создание объекта виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="bfec5-109">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="bfec5-110">Первая команда получает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="bfec5-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="bfec5-111">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bfec5-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="bfec5-112">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bfec5-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="bfec5-113">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="bfec5-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="bfec5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bfec5-114">PARAMETERS</span></span>

### <span data-ttu-id="bfec5-115">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="bfec5-115">-AvailabilitySetId</span></span>
<span data-ttu-id="bfec5-116">Указывает идентификатор группы доступности.</span><span class="sxs-lookup"><span data-stu-id="bfec5-116">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="bfec5-117">Чтобы получить объект группы доступности, используйте командлет Get-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="bfec5-117">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="bfec5-118">Объект "набор доступности" имеет свойство ID.</span><span class="sxs-lookup"><span data-stu-id="bfec5-118">The availability set object contains an ID property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfec5-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="bfec5-119">-IdentityType</span></span>
<span data-ttu-id="bfec5-120">Удостоверение виртуальной машины, если она настроена.</span><span class="sxs-lookup"><span data-stu-id="bfec5-120">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfec5-121">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="bfec5-121">-LicenseType</span></span>
<span data-ttu-id="bfec5-122">Тип лицензии, предназначенный для использования собственного сценария лицензирования.</span><span class="sxs-lookup"><span data-stu-id="bfec5-122">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfec5-123">-Теги</span><span class="sxs-lookup"><span data-stu-id="bfec5-123">-Tags</span></span>
<span data-ttu-id="bfec5-124">Теги, вложенные в ресурс.</span><span class="sxs-lookup"><span data-stu-id="bfec5-124">The tags attached to the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfec5-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="bfec5-125">-VMName</span></span>
<span data-ttu-id="bfec5-126">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bfec5-126">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfec5-127">-VMSize</span><span class="sxs-lookup"><span data-stu-id="bfec5-127">-VMSize</span></span>
<span data-ttu-id="bfec5-128">Задает размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bfec5-128">Specifies the size for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfec5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfec5-129">CommonParameters</span></span>
<span data-ttu-id="bfec5-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bfec5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfec5-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfec5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfec5-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bfec5-132">INPUTS</span></span>

### <span data-ttu-id="bfec5-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="bfec5-133">None</span></span>
<span data-ttu-id="bfec5-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="bfec5-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bfec5-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfec5-135">OUTPUTS</span></span>

## <span data-ttu-id="bfec5-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="bfec5-136">NOTES</span></span>

## <span data-ttu-id="bfec5-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfec5-137">RELATED LINKS</span></span>

[<span data-ttu-id="bfec5-138">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="bfec5-138">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="bfec5-139">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="bfec5-139">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="bfec5-140">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="bfec5-140">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="bfec5-141">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="bfec5-141">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


