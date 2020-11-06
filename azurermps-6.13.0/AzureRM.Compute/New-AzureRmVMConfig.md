---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 6809088110944648781fc2264bd2c56f98cbee1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566546"
---
# <span data-ttu-id="c1cb8-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="c1cb8-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="c1cb8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="c1cb8-103">Создание настраиваемого объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1cb8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1cb8-104">SYNTAX</span></span>

### <span data-ttu-id="c1cb8-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c1cb8-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1cb8-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1cb8-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1cb8-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1cb8-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1cb8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1cb8-108">DESCRIPTION</span></span>
<span data-ttu-id="c1cb8-109">Командлет **New-AzureRmVMConfig** создает настраиваемый локальный объект виртуальной машины для Azure.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-109">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="c1cb8-110">Другие командлеты можно использовать для настройки объекта виртуальной машины, например Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface и Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="c1cb8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1cb8-111">EXAMPLES</span></span>

### <span data-ttu-id="c1cb8-112">Пример 1: создание объекта виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="c1cb8-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="c1cb8-113">Первая команда получает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="c1cb8-114">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="c1cb8-115">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="c1cb8-116">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="c1cb8-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1cb8-117">PARAMETERS</span></span>

### <span data-ttu-id="c1cb8-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c1cb8-118">-AssignIdentity</span></span>
<span data-ttu-id="c1cb8-119">Укажите учетную запись, назначенную системой для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-119">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1cb8-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="c1cb8-120">-AvailabilitySetId</span></span>
<span data-ttu-id="c1cb8-121">Указывает идентификатор группы доступности.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="c1cb8-122">Чтобы получить объект группы доступности, используйте командлет Get-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-122">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="c1cb8-123">Объект "набор доступности" имеет свойство ID.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-123">The availability set object contains an ID property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cb8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1cb8-124">-DefaultProfile</span></span>
<span data-ttu-id="c1cb8-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1cb8-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="c1cb8-126">-EnableUltraSSD</span></span>
<span data-ttu-id="c1cb8-127">Позволяет иметь возможность использовать один или несколько дисков управляемых данных с типом учетной записи хранения UltraSSD_LRS на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="c1cb8-128">Управляемые диски с типом учетной записи хранения UltraSSD_LRS можно добавлять на виртуальную машину только в том случае, если включено это свойство.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cb8-129">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="c1cb8-129">-IdentityId</span></span>
<span data-ttu-id="c1cb8-130">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="c1cb8-131">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="c1cb8-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cb8-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c1cb8-132">-IdentityType</span></span>
<span data-ttu-id="c1cb8-133">Удостоверение виртуальной машины, если она настроена.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-133">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1cb8-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c1cb8-134">-LicenseType</span></span>
<span data-ttu-id="c1cb8-135">Тип лицензии, предназначенный для использования собственного сценария лицензирования.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-135">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1cb8-136">-Теги</span><span class="sxs-lookup"><span data-stu-id="c1cb8-136">-Tags</span></span>
<span data-ttu-id="c1cb8-137">Теги, вложенные в ресурс.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-137">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cb8-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="c1cb8-138">-VMName</span></span>
<span data-ttu-id="c1cb8-139">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-139">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cb8-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="c1cb8-140">-VMSize</span></span>
<span data-ttu-id="c1cb8-141">Задает размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-141">Specifies the size for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cb8-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="c1cb8-142">-Zone</span></span>
<span data-ttu-id="c1cb8-143">Указывает список зон для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-143">Specifies the zone list for the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cb8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1cb8-144">CommonParameters</span></span>
<span data-ttu-id="c1cb8-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1cb8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1cb8-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1cb8-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1cb8-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1cb8-147">INPUTS</span></span>

### <span data-ttu-id="c1cb8-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c1cb8-148">System.String</span></span>

### <span data-ttu-id="c1cb8-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="c1cb8-149">System.String[]</span></span>

### <span data-ttu-id="c1cb8-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c1cb8-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c1cb8-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1cb8-151">OUTPUTS</span></span>

### <span data-ttu-id="c1cb8-152">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c1cb8-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c1cb8-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1cb8-153">NOTES</span></span>

## <span data-ttu-id="c1cb8-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1cb8-154">RELATED LINKS</span></span>

[<span data-ttu-id="c1cb8-155">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c1cb8-155">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="c1cb8-156">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c1cb8-156">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="c1cb8-157">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="c1cb8-157">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="c1cb8-158">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c1cb8-158">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


