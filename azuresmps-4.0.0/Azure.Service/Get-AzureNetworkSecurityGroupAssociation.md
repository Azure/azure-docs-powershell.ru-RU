---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 6AF7D392-8C8B-4695-95D0-E927093F654A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21eb1b7bcad200e67659f830bfb3bbef42fe0f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076582"
---
# <span data-ttu-id="07ab6-101">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="07ab6-101">Get-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="07ab6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07ab6-102">SYNOPSIS</span></span>
<span data-ttu-id="07ab6-103">Получает сетевую группу безопасности для виртуальной машины, сетевого адаптера или роли PaaS.</span><span class="sxs-lookup"><span data-stu-id="07ab6-103">Gets a network security group for a virtual machine, network adapter, or PaaS role.</span></span>

## <span data-ttu-id="07ab6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07ab6-104">SYNTAX</span></span>

### <span data-ttu-id="07ab6-105">GetNetworkSecurityGroupAssociationForSubnet</span><span class="sxs-lookup"><span data-stu-id="07ab6-105">GetNetworkSecurityGroupAssociationForSubnet</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="07ab6-106">GetNetworkSecurityGroupAssociationForIaaSRole</span><span class="sxs-lookup"><span data-stu-id="07ab6-106">GetNetworkSecurityGroupAssociationForIaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="07ab6-107">GetNetworkSecurityGroupAssociationForPaaSRole</span><span class="sxs-lookup"><span data-stu-id="07ab6-107">GetNetworkSecurityGroupAssociationForPaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation [-Slot <String>] -RoleName <String> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="07ab6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07ab6-108">DESCRIPTION</span></span>
<span data-ttu-id="07ab6-109">Командлет **Get-AzureNetworkSecurityGroupAssociation** получает сетевую группу безопасности для виртуальной машины, сетевого адаптера или платформы как роль службы (PaaS).</span><span class="sxs-lookup"><span data-stu-id="07ab6-109">The **Get-AzureNetworkSecurityGroupAssociation** cmdlet gets the network security group for a virtual machine, network adapter, or platform as a service (PaaS) role.</span></span>

## <span data-ttu-id="07ab6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07ab6-110">EXAMPLES</span></span>

### <span data-ttu-id="07ab6-111">Пример 1: получение группы безопасности сети для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="07ab6-111">Example 1: Get the network security group for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureNetworkSecurityGroupAssociation
```

<span data-ttu-id="07ab6-112">Эта команда получает виртуальную машину с именем ContosoVM06 для службы с именем ContosoService и передает этот объект виртуальной машины в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="07ab6-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="07ab6-113">Текущий командлет получает сетевую группу безопасности, связанную с этой виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="07ab6-113">The current cmdlet gets the network security group associated to that virtual machine.</span></span>

## <span data-ttu-id="07ab6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07ab6-114">PARAMETERS</span></span>

### <span data-ttu-id="07ab6-115">-Подробно</span><span class="sxs-lookup"><span data-stu-id="07ab6-115">-Detailed</span></span>
<span data-ttu-id="07ab6-116">Указывает на то, что этот командлет возвращает сведения о сетевой группе безопасности, связанной с виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="07ab6-116">Indicates that this cmdlet returns details of the network security group that is associated to the virtual machine.</span></span>
<span data-ttu-id="07ab6-117">Эти сведения включают расположение и правила.</span><span class="sxs-lookup"><span data-stu-id="07ab6-117">These details include location and rules.</span></span>

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

### <span data-ttu-id="07ab6-118">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="07ab6-118">-NetworkInterfaceName</span></span>
<span data-ttu-id="07ab6-119">Указывает имя сетевого адаптера, для которого этот командлет получает сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="07ab6-119">Specifies the name of the network adapter for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07ab6-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="07ab6-120">-Profile</span></span>
<span data-ttu-id="07ab6-121">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="07ab6-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="07ab6-122">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="07ab6-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="07ab6-123">-RoleName</span><span class="sxs-lookup"><span data-stu-id="07ab6-123">-RoleName</span></span>
<span data-ttu-id="07ab6-124">Указывает имя роли PaaS, для которой этот командлет получает сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="07ab6-124">Specifies the name of a PaaS role for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07ab6-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="07ab6-125">-ServiceName</span></span>
<span data-ttu-id="07ab6-126">Указывает имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="07ab6-126">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="07ab6-127">Роль PaaS принадлежит службе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="07ab6-127">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07ab6-128">-Slot</span><span class="sxs-lookup"><span data-stu-id="07ab6-128">-Slot</span></span>
<span data-ttu-id="07ab6-129">Указывает гнездо PaaS.</span><span class="sxs-lookup"><span data-stu-id="07ab6-129">Specifies a PaaS slot.</span></span>
<span data-ttu-id="07ab6-130">Роль PaaS, для которой этот командлет получает сетевую группу безопасности, имеет область, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="07ab6-130">The PaaS role for which this cmdlet gets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="07ab6-131">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="07ab6-131">Valid values are:</span></span> 

- <span data-ttu-id="07ab6-132">Спецификации</span><span class="sxs-lookup"><span data-stu-id="07ab6-132">Production</span></span>
- <span data-ttu-id="07ab6-133">Промежуточного хранения</span><span class="sxs-lookup"><span data-stu-id="07ab6-133">Staging</span></span> 

<span data-ttu-id="07ab6-134">Значением по умолчанию является "производство".</span><span class="sxs-lookup"><span data-stu-id="07ab6-134">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ab6-135">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="07ab6-135">-SubnetName</span></span>
<span data-ttu-id="07ab6-136">Указывает имя подсети, для которой этот командлет получает сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="07ab6-136">Specifies the name of a subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ab6-137">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="07ab6-137">-VirtualNetworkName</span></span>
<span data-ttu-id="07ab6-138">Указывает имя виртуальной сети, содержащей подсеть, для которой этот командлет получает сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="07ab6-138">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ab6-139">-VM</span><span class="sxs-lookup"><span data-stu-id="07ab6-139">-VM</span></span>
<span data-ttu-id="07ab6-140">Указывает виртуальную машину, к которой этот командлет применяет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="07ab6-140">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07ab6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ab6-141">CommonParameters</span></span>
<span data-ttu-id="07ab6-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07ab6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ab6-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07ab6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ab6-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07ab6-144">INPUTS</span></span>

## <span data-ttu-id="07ab6-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07ab6-145">OUTPUTS</span></span>

### <span data-ttu-id="07ab6-146">Microsoft. WindowsAzure. Commands. ServiceManagement. Network. NetworkSecurityGroup. Model. INetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="07ab6-146">Microsoft.WindowsAzure.Commands.ServiceManagement.Network.NetworkSecurityGroup.Model.INetworkSecurityGroup</span></span>

## <span data-ttu-id="07ab6-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="07ab6-147">NOTES</span></span>

## <span data-ttu-id="07ab6-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07ab6-148">RELATED LINKS</span></span>

[<span data-ttu-id="07ab6-149">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="07ab6-149">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="07ab6-150">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="07ab6-150">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)


