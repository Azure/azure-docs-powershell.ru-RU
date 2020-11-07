---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 4b128346d77e090e5b0699ace8f03eaa9a4786a1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911462"
---
# <span data-ttu-id="e13c2-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="e13c2-101">New-AzVMConfig</span></span>

## <span data-ttu-id="e13c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e13c2-102">SYNOPSIS</span></span>
<span data-ttu-id="e13c2-103">Создание настраиваемого объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e13c2-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="e13c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e13c2-104">SYNTAX</span></span>

### <span data-ttu-id="e13c2-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e13c2-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e13c2-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="e13c2-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e13c2-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="e13c2-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e13c2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e13c2-108">DESCRIPTION</span></span>
<span data-ttu-id="e13c2-109">Командлет **New-AzVMConfig** создает настраиваемый локальный объект виртуальной машины для Azure.</span><span class="sxs-lookup"><span data-stu-id="e13c2-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="e13c2-110">Другие командлеты можно использовать для настройки объекта виртуальной машины, например Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface и Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="e13c2-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="e13c2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e13c2-111">EXAMPLES</span></span>

### <span data-ttu-id="e13c2-112">Пример 1: создание объекта виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="e13c2-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="e13c2-113">Первая команда получает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e13c2-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="e13c2-114">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e13c2-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e13c2-115">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e13c2-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e13c2-116">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e13c2-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="e13c2-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e13c2-117">PARAMETERS</span></span>

### <span data-ttu-id="e13c2-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e13c2-118">-AssignIdentity</span></span>
<span data-ttu-id="e13c2-119">Укажите учетную запись, назначенную системой для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e13c2-119">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e13c2-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="e13c2-120">-AvailabilitySetId</span></span>
<span data-ttu-id="e13c2-121">Указывает идентификатор группы доступности.</span><span class="sxs-lookup"><span data-stu-id="e13c2-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="e13c2-122">Чтобы получить объект группы доступности, используйте командлет Get-AzAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e13c2-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="e13c2-123">Объект "набор доступности" имеет свойство ID.</span><span class="sxs-lookup"><span data-stu-id="e13c2-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="e13c2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e13c2-124">-DefaultProfile</span></span>
<span data-ttu-id="e13c2-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e13c2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e13c2-126">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="e13c2-126">-IdentityId</span></span>
<span data-ttu-id="e13c2-127">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="e13c2-127">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="e13c2-128">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="e13c2-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e13c2-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e13c2-129">-IdentityType</span></span>
<span data-ttu-id="e13c2-130">Удостоверение виртуальной машины, если она настроена.</span><span class="sxs-lookup"><span data-stu-id="e13c2-130">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e13c2-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e13c2-131">-LicenseType</span></span>
<span data-ttu-id="e13c2-132">Тип лицензии, предназначенный для использования собственного сценария лицензирования.</span><span class="sxs-lookup"><span data-stu-id="e13c2-132">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e13c2-133">-Теги</span><span class="sxs-lookup"><span data-stu-id="e13c2-133">-Tags</span></span>
<span data-ttu-id="e13c2-134">Теги, вложенные в ресурс.</span><span class="sxs-lookup"><span data-stu-id="e13c2-134">The tags attached to the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e13c2-135">-VMName</span><span class="sxs-lookup"><span data-stu-id="e13c2-135">-VMName</span></span>
<span data-ttu-id="e13c2-136">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e13c2-136">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="e13c2-137">-VMSize</span><span class="sxs-lookup"><span data-stu-id="e13c2-137">-VMSize</span></span>
<span data-ttu-id="e13c2-138">Задает размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e13c2-138">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="e13c2-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="e13c2-139">-Zone</span></span>
<span data-ttu-id="e13c2-140">Указывает список зон для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e13c2-140">Specifies the zone list for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e13c2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e13c2-141">CommonParameters</span></span>
<span data-ttu-id="e13c2-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e13c2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e13c2-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e13c2-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e13c2-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e13c2-144">INPUTS</span></span>

### <span data-ttu-id="e13c2-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="e13c2-145">None</span></span>
<span data-ttu-id="e13c2-146">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e13c2-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e13c2-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e13c2-147">OUTPUTS</span></span>

### <span data-ttu-id="e13c2-148">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e13c2-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e13c2-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="e13c2-149">NOTES</span></span>

## <span data-ttu-id="e13c2-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e13c2-150">RELATED LINKS</span></span>

[<span data-ttu-id="e13c2-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e13c2-151">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="e13c2-152">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e13c2-152">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="e13c2-153">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="e13c2-153">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="e13c2-154">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e13c2-154">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


