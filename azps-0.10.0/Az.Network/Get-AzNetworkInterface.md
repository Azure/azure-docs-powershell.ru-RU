---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
ms.openlocfilehash: df769ff4a6e4eb47bc47b881ac8c06de1fdb9e4c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909953"
---
# <span data-ttu-id="4af44-101">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4af44-101">Get-AzNetworkInterface</span></span>

## <span data-ttu-id="4af44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4af44-102">SYNOPSIS</span></span>
<span data-ttu-id="4af44-103">Возвращает сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="4af44-103">Gets a network interface.</span></span>

## <span data-ttu-id="4af44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4af44-104">SYNTAX</span></span>

### <span data-ttu-id="4af44-105">NoExpandStandAloneNic (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4af44-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4af44-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="4af44-106">ExpandStandAloneNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4af44-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="4af44-107">NoExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4af44-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="4af44-108">ExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4af44-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4af44-109">DESCRIPTION</span></span>
<span data-ttu-id="4af44-110">Командлет **Get-AzNetworkInterface** получает сетевой интерфейс Azure или список сетевых интерфейсов Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4af44-110">The **Get-AzNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="4af44-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4af44-111">EXAMPLES</span></span>

### <span data-ttu-id="4af44-112">Пример 1: получение всех сетевых интерфейсов</span><span class="sxs-lookup"><span data-stu-id="4af44-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzNetworkInterface
```

<span data-ttu-id="4af44-113">Эта команда получает все сетевые интерфейсы для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="4af44-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="4af44-114">Пример 2: получение всех сетевых интерфейсов с определенным состоянием подготовки</span><span class="sxs-lookup"><span data-stu-id="4af44-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="4af44-115">Эта команда получает все сетевые интерфейсы в группе ресурсов с именем ResourceGroup1, для которой успешно определено состояние подготовки.</span><span class="sxs-lookup"><span data-stu-id="4af44-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="4af44-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4af44-116">PARAMETERS</span></span>

### <span data-ttu-id="4af44-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af44-117">-DefaultProfile</span></span>
<span data-ttu-id="4af44-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4af44-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4af44-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4af44-119">-ExpandResource</span></span>
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

### <span data-ttu-id="4af44-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4af44-120">-Name</span></span>
<span data-ttu-id="4af44-121">Указывает имя сетевого интерфейса, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4af44-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4af44-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4af44-122">-ResourceGroupName</span></span>
<span data-ttu-id="4af44-123">Указывает имя группы ресурсов, из которой этот командлет получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="4af44-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="4af44-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="4af44-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="4af44-125">Указывает индекс виртуальной машины в наборе масштабов виртуальных машин, на основе которого этот командлет получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="4af44-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="4af44-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4af44-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="4af44-127">Указывает имя набора масштабов виртуальной машины, на основе которого этот командлет получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="4af44-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="4af44-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af44-128">CommonParameters</span></span>
<span data-ttu-id="4af44-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4af44-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af44-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4af44-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af44-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4af44-131">INPUTS</span></span>

## <span data-ttu-id="4af44-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4af44-132">OUTPUTS</span></span>

### <span data-ttu-id="4af44-133">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4af44-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="4af44-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="4af44-134">NOTES</span></span>

## <span data-ttu-id="4af44-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4af44-135">RELATED LINKS</span></span>

[<span data-ttu-id="4af44-136">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4af44-136">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="4af44-137">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4af44-137">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="4af44-138">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4af44-138">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


