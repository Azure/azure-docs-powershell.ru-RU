---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 263293ea117f85caf32029ee0cfbf0dff2142cc3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915177"
---
# <span data-ttu-id="07f91-101">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="07f91-101">Get-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="07f91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07f91-102">SYNOPSIS</span></span>
<span data-ttu-id="07f91-103">Возвращает сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="07f91-103">Gets a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07f91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07f91-104">SYNTAX</span></span>

### <span data-ttu-id="07f91-105">NoExpandStandAloneNic (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07f91-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07f91-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="07f91-106">ExpandStandAloneNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07f91-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="07f91-107">NoExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07f91-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="07f91-108">ExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07f91-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07f91-109">DESCRIPTION</span></span>
<span data-ttu-id="07f91-110">Командлет **Get-AzureRmNetworkInterface** получает сетевой интерфейс Azure или список сетевых интерфейсов Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07f91-110">The **Get-AzureRmNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="07f91-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07f91-111">EXAMPLES</span></span>

### <span data-ttu-id="07f91-112">Пример 1: получение всех сетевых интерфейсов</span><span class="sxs-lookup"><span data-stu-id="07f91-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzureRmNetworkInterface
```

<span data-ttu-id="07f91-113">Эта команда получает все сетевые интерфейсы для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="07f91-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="07f91-114">Пример 2: получение всех сетевых интерфейсов с определенным состоянием подготовки</span><span class="sxs-lookup"><span data-stu-id="07f91-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="07f91-115">Эта команда получает все сетевые интерфейсы в группе ресурсов с именем ResourceGroup1, для которой успешно определено состояние подготовки.</span><span class="sxs-lookup"><span data-stu-id="07f91-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="07f91-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07f91-116">PARAMETERS</span></span>

### <span data-ttu-id="07f91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f91-117">-DefaultProfile</span></span>
<span data-ttu-id="07f91-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07f91-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07f91-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="07f91-119">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07f91-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07f91-120">-Name</span></span>
<span data-ttu-id="07f91-121">Указывает имя сетевого интерфейса, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="07f91-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07f91-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f91-122">-ResourceGroupName</span></span>
<span data-ttu-id="07f91-123">Указывает имя группы ресурсов, из которой этот командлет получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="07f91-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07f91-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="07f91-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="07f91-125">Указывает индекс виртуальной машины в наборе масштабов виртуальных машин, на основе которого этот командлет получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="07f91-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07f91-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="07f91-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="07f91-127">Указывает имя набора масштабов виртуальной машины, на основе которого этот командлет получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="07f91-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07f91-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f91-128">CommonParameters</span></span>
<span data-ttu-id="07f91-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07f91-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f91-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07f91-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f91-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07f91-131">INPUTS</span></span>

## <span data-ttu-id="07f91-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07f91-132">OUTPUTS</span></span>

### <span data-ttu-id="07f91-133">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="07f91-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="07f91-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="07f91-134">NOTES</span></span>

## <span data-ttu-id="07f91-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07f91-135">RELATED LINKS</span></span>

[<span data-ttu-id="07f91-136">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="07f91-136">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="07f91-137">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="07f91-137">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="07f91-138">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="07f91-138">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


