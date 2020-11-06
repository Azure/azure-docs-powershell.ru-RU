---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
ms.openlocfilehash: 00384e7765ec0ef47789a6ed1efa6c529bea10b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569932"
---
# <span data-ttu-id="49583-101">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="49583-101">Get-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="49583-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49583-102">SYNOPSIS</span></span>
<span data-ttu-id="49583-103">Возвращает сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="49583-103">Gets a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49583-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49583-104">SYNTAX</span></span>

### <span data-ttu-id="49583-105">NoExpandStandAloneNic (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49583-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49583-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="49583-106">ExpandStandAloneNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49583-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="49583-107">NoExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49583-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="49583-108">ExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49583-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49583-109">DESCRIPTION</span></span>
<span data-ttu-id="49583-110">Командлет **Get-AzureRmNetworkInterface** получает сетевой интерфейс Azure или список сетевых интерфейсов Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49583-110">The **Get-AzureRmNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="49583-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49583-111">EXAMPLES</span></span>

### <span data-ttu-id="49583-112">Пример 1: получение всех сетевых интерфейсов</span><span class="sxs-lookup"><span data-stu-id="49583-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzureRmNetworkInterface
```

<span data-ttu-id="49583-113">Эта команда получает все сетевые интерфейсы для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="49583-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="49583-114">Пример 2: получение всех сетевых интерфейсов с определенным состоянием подготовки</span><span class="sxs-lookup"><span data-stu-id="49583-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="49583-115">Эта команда получает все сетевые интерфейсы в группе ресурсов с именем ResourceGroup1, для которой успешно определено состояние подготовки.</span><span class="sxs-lookup"><span data-stu-id="49583-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="49583-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49583-116">PARAMETERS</span></span>

### <span data-ttu-id="49583-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49583-117">-DefaultProfile</span></span>
<span data-ttu-id="49583-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49583-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49583-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="49583-119">-ExpandResource</span></span>
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

### <span data-ttu-id="49583-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49583-120">-Name</span></span>
<span data-ttu-id="49583-121">Указывает имя сетевого интерфейса, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="49583-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

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

### <span data-ttu-id="49583-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49583-122">-ResourceGroupName</span></span>
<span data-ttu-id="49583-123">Указывает имя группы ресурсов, из которой этот командлет получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="49583-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="49583-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="49583-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="49583-125">Указывает индекс виртуальной машины в наборе масштабов виртуальных машин, на основе которого этот командлет получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="49583-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="49583-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="49583-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="49583-127">Указывает имя набора масштабов виртуальной машины, на основе которого этот командлет получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="49583-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="49583-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49583-128">CommonParameters</span></span>
<span data-ttu-id="49583-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49583-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49583-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49583-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49583-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49583-131">INPUTS</span></span>

### <span data-ttu-id="49583-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="49583-132">None</span></span>
<span data-ttu-id="49583-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="49583-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49583-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49583-134">OUTPUTS</span></span>

### <span data-ttu-id="49583-135">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="49583-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="49583-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="49583-136">NOTES</span></span>

## <span data-ttu-id="49583-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49583-137">RELATED LINKS</span></span>

[<span data-ttu-id="49583-138">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="49583-138">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="49583-139">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="49583-139">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="49583-140">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="49583-140">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


