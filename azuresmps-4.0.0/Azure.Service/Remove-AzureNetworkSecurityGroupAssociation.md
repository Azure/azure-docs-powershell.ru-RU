---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E3E0237-8E2D-4B3A-AD0C-2121DDE1AAB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28259b97f382092f5e6293048c040688011cfe92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076152"
---
# <span data-ttu-id="6f2d7-101">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="6f2d7-101">Remove-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="6f2d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f2d7-102">SYNOPSIS</span></span>
<span data-ttu-id="6f2d7-103">Удаляет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-103">Removes a network security group.</span></span>

## <span data-ttu-id="6f2d7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f2d7-104">SYNTAX</span></span>

### <span data-ttu-id="6f2d7-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span><span class="sxs-lookup"><span data-stu-id="6f2d7-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6f2d7-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span><span class="sxs-lookup"><span data-stu-id="6f2d7-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6f2d7-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span><span class="sxs-lookup"><span data-stu-id="6f2d7-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> [-Slot <String>] -RoleName <String>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f2d7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f2d7-108">DESCRIPTION</span></span>
<span data-ttu-id="6f2d7-109">Командлет **Remove-AzureNetworkSecurityGroupAssociation** удаляет группу безопасности сети из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-109">The **Remove-AzureNetworkSecurityGroupAssociation** cmdlet removes a network security group from a virtual machine.</span></span>

## <span data-ttu-id="6f2d7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f2d7-110">EXAMPLES</span></span>

### <span data-ttu-id="6f2d7-111">Пример 1: Удаление виртуальной машины в сетевую группу безопасности</span><span class="sxs-lookup"><span data-stu-id="6f2d7-111">Example 1: Remove a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Remove-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="6f2d7-112">Эта команда получает виртуальную машину с именем ContosoVM06 для службы с именем ContosoService и передает этот объект виртуальной машины в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="6f2d7-113">Текущий командлет удаляет группу безопасности сети с именем ContosoNetworkSecurityGroup из этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-113">The current cmdlet removes the network security group named ContosoNetworkSecurityGroup from that virtual machine.</span></span>

## <span data-ttu-id="6f2d7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f2d7-114">PARAMETERS</span></span>

### <span data-ttu-id="6f2d7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6f2d7-115">-Force</span></span>
<span data-ttu-id="6f2d7-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6f2d7-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f2d7-117">-Name</span></span>
<span data-ttu-id="6f2d7-118">Указывает имя сетевой группы безопасности, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2d7-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="6f2d7-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="6f2d7-120">Указывает имя сетевого адаптера, с которого этот командлет удаляет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-120">Specifies the name of the network adapter from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f2d7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f2d7-121">-PassThru</span></span>
<span data-ttu-id="6f2d7-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6f2d7-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6f2d7-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="6f2d7-124">-Profile</span></span>
<span data-ttu-id="6f2d7-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6f2d7-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2d7-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="6f2d7-127">-RoleName</span></span>
<span data-ttu-id="6f2d7-128">Указывает имя роли PaaS, из которой этот командлет удаляет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-128">Specifies the name of a PaaS role from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f2d7-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6f2d7-129">-ServiceName</span></span>
<span data-ttu-id="6f2d7-130">Указывает имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="6f2d7-131">Роль PaaS, из которой этот командлет удаляет сетевую группу безопасности, принадлежит службе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-131">The PaaS role from which this cmdlet removes a network security group belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f2d7-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="6f2d7-132">-Slot</span></span>
<span data-ttu-id="6f2d7-133">Указывает гнездо PaaS.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="6f2d7-134">Роль PaaS, из которой этот командлет удаляет сетевую группу безопасности, имеет область, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-134">The PaaS role from which this cmdlet removes a network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="6f2d7-135">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="6f2d7-135">Valid values are:</span></span>

- <span data-ttu-id="6f2d7-136">Спецификации</span><span class="sxs-lookup"><span data-stu-id="6f2d7-136">Production</span></span>
- <span data-ttu-id="6f2d7-137">Промежуточного хранения</span><span class="sxs-lookup"><span data-stu-id="6f2d7-137">Staging</span></span>

<span data-ttu-id="6f2d7-138">Значением по умолчанию является "производство".</span><span class="sxs-lookup"><span data-stu-id="6f2d7-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2d7-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="6f2d7-139">-SubnetName</span></span>
<span data-ttu-id="6f2d7-140">Указывает имя подсети, из которой этот командлет удаляет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-140">Specifies the name of a subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2d7-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="6f2d7-141">-VirtualNetworkName</span></span>
<span data-ttu-id="6f2d7-142">Указывает имя виртуальной сети, содержащей подсеть, из которой этот командлет удаляет группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-142">Specifies the name of a virtual network that contains the subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2d7-143">-VM</span><span class="sxs-lookup"><span data-stu-id="6f2d7-143">-VM</span></span>
<span data-ttu-id="6f2d7-144">Указывает виртуальную машину, к которой этот командлет применяет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f2d7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f2d7-145">CommonParameters</span></span>
<span data-ttu-id="6f2d7-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f2d7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f2d7-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f2d7-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f2d7-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f2d7-148">INPUTS</span></span>

## <span data-ttu-id="6f2d7-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f2d7-149">OUTPUTS</span></span>

### <span data-ttu-id="6f2d7-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f2d7-150">System.Boolean</span></span>

## <span data-ttu-id="6f2d7-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f2d7-151">NOTES</span></span>

## <span data-ttu-id="6f2d7-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f2d7-152">RELATED LINKS</span></span>

[<span data-ttu-id="6f2d7-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="6f2d7-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="6f2d7-154">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="6f2d7-154">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)
