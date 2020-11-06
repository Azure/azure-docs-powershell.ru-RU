---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 0e5216f88cc860244cf11a693a73e30ba6e83390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566586"
---
# <span data-ttu-id="9ecc6-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9ecc6-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="9ecc6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ecc6-102">SYNOPSIS</span></span>
<span data-ttu-id="9ecc6-103">Создает конфигурацию зонда для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ecc6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ecc6-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ecc6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ecc6-105">DESCRIPTION</span></span>
<span data-ttu-id="9ecc6-106">Командлет **New-AzureRmLoadBalancerProbeConfig** создает конфигурацию зонда для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="9ecc6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ecc6-107">EXAMPLES</span></span>

### <span data-ttu-id="9ecc6-108">Пример 1: создание конфигурации зонда</span><span class="sxs-lookup"><span data-stu-id="9ecc6-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="9ecc6-109">Эта команда создает конфигурацию зонда с именем MyProbe, используя HTTP-протокол.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="9ecc6-110">Новый зонд будет подключаться к службе балансировки нагрузки на порте 80.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="9ecc6-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ecc6-111">PARAMETERS</span></span>

### <span data-ttu-id="9ecc6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ecc6-112">-DefaultProfile</span></span>
<span data-ttu-id="9ecc6-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ecc6-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9ecc6-114">-IntervalInSeconds</span></span>
<span data-ttu-id="9ecc6-115">Задает интервал (в секундах) между зондами каждого экземпляра службы с балансировкой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ecc6-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9ecc6-116">-Name</span></span>
<span data-ttu-id="9ecc6-117">Указывает имя конфигурации зонда, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="9ecc6-118">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="9ecc6-118">-Port</span></span>
<span data-ttu-id="9ecc6-119">Указывает порт, на котором новый зонд должен подключаться к службе балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ecc6-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="9ecc6-120">-ProbeCount</span></span>
<span data-ttu-id="9ecc6-121">Задает количество последовательных сбоев каждого экземпляра, которое считается неработоспособным для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ecc6-122">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="9ecc6-122">-Protocol</span></span>
<span data-ttu-id="9ecc6-123">Указывает протокол, используемый для конфигурации пробы.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="9ecc6-124">Допустимые значения этого параметра: TCP или HTTP.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ecc6-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="9ecc6-125">-RequestPath</span></span>
<span data-ttu-id="9ecc6-126">Указывает путь в службе балансировки нагрузки для проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="9ecc6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ecc6-127">CommonParameters</span></span>
<span data-ttu-id="9ecc6-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ecc6-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ecc6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ecc6-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ecc6-130">INPUTS</span></span>

### <span data-ttu-id="9ecc6-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="9ecc6-131">None</span></span>
<span data-ttu-id="9ecc6-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9ecc6-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9ecc6-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ecc6-133">OUTPUTS</span></span>

### <span data-ttu-id="9ecc6-134">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="9ecc6-134">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="9ecc6-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ecc6-135">NOTES</span></span>

## <span data-ttu-id="9ecc6-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ecc6-136">RELATED LINKS</span></span>

[<span data-ttu-id="9ecc6-137">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9ecc6-137">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="9ecc6-138">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9ecc6-138">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="9ecc6-139">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9ecc6-139">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="9ecc6-140">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9ecc6-140">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


