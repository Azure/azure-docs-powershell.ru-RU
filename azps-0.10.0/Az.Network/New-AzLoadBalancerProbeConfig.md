---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 6e647cbc20e74c5c473fe91b2ec592177c0713ba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909673"
---
# <span data-ttu-id="cefdd-101">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cefdd-101">New-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="cefdd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cefdd-102">SYNOPSIS</span></span>
<span data-ttu-id="cefdd-103">Создает конфигурацию зонда для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="cefdd-103">Creates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="cefdd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cefdd-104">SYNTAX</span></span>

```
New-AzLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cefdd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cefdd-105">DESCRIPTION</span></span>
<span data-ttu-id="cefdd-106">Командлет **New-AzLoadBalancerProbeConfig** создает конфигурацию зонда для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="cefdd-106">The **New-AzLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="cefdd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cefdd-107">EXAMPLES</span></span>

### <span data-ttu-id="cefdd-108">Пример 1: создание конфигурации зонда</span><span class="sxs-lookup"><span data-stu-id="cefdd-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="cefdd-109">Эта команда создает конфигурацию зонда с именем MyProbe, используя HTTP-протокол.</span><span class="sxs-lookup"><span data-stu-id="cefdd-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="cefdd-110">Новый зонд будет подключаться к службе балансировки нагрузки на порте 80.</span><span class="sxs-lookup"><span data-stu-id="cefdd-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="cefdd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cefdd-111">PARAMETERS</span></span>

### <span data-ttu-id="cefdd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cefdd-112">-DefaultProfile</span></span>
<span data-ttu-id="cefdd-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cefdd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cefdd-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="cefdd-114">-IntervalInSeconds</span></span>
<span data-ttu-id="cefdd-115">Задает интервал (в секундах) между зондами каждого экземпляра службы с балансировкой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="cefdd-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="cefdd-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cefdd-116">-Name</span></span>
<span data-ttu-id="cefdd-117">Указывает имя конфигурации зонда, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="cefdd-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="cefdd-118">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="cefdd-118">-Port</span></span>
<span data-ttu-id="cefdd-119">Указывает порт, на котором новый зонд должен подключаться к службе балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="cefdd-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="cefdd-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="cefdd-120">-ProbeCount</span></span>
<span data-ttu-id="cefdd-121">Задает количество последовательных сбоев каждого экземпляра, которое считается неработоспособным для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cefdd-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="cefdd-122">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="cefdd-122">-Protocol</span></span>
<span data-ttu-id="cefdd-123">Указывает протокол, используемый для конфигурации пробы.</span><span class="sxs-lookup"><span data-stu-id="cefdd-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="cefdd-124">Допустимые значения этого параметра: TCP или HTTP.</span><span class="sxs-lookup"><span data-stu-id="cefdd-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="cefdd-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="cefdd-125">-RequestPath</span></span>
<span data-ttu-id="cefdd-126">Указывает путь в службе балансировки нагрузки для проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="cefdd-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="cefdd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cefdd-127">CommonParameters</span></span>
<span data-ttu-id="cefdd-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cefdd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cefdd-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cefdd-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cefdd-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cefdd-130">INPUTS</span></span>

## <span data-ttu-id="cefdd-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cefdd-131">OUTPUTS</span></span>

### <span data-ttu-id="cefdd-132">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="cefdd-132">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="cefdd-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="cefdd-133">NOTES</span></span>

## <span data-ttu-id="cefdd-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cefdd-134">RELATED LINKS</span></span>

[<span data-ttu-id="cefdd-135">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cefdd-135">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="cefdd-136">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cefdd-136">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="cefdd-137">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cefdd-137">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="cefdd-138">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cefdd-138">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


