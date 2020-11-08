---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorprotocolconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
ms.openlocfilehash: 5a0994a5328390a928fd60cda8e8004deaaab162
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065488"
---
# <span data-ttu-id="5676d-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="5676d-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span></span>

## <span data-ttu-id="5676d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5676d-102">SYNOPSIS</span></span>
<span data-ttu-id="5676d-103">Создание конфигурации протокола, используемой для оценки тестов по протоколу TCP, HTTP или ICMP.</span><span class="sxs-lookup"><span data-stu-id="5676d-103">Create protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="5676d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5676d-104">SYNTAX</span></span>

### <span data-ttu-id="5676d-105">Номера</span><span class="sxs-lookup"><span data-stu-id="5676d-105">TCP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-TcpProtocol] -Port <Int32>
 [-DisableTraceRoute] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5676d-106">ЧЕРЕЗ</span><span class="sxs-lookup"><span data-stu-id="5676d-106">HTTP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-HttpProtocol] [-Port <Int32>]
 [-Method <String>] [-Path <String>] [-RequestHeader <Hashtable>] [-ValidStatusCodeRange <String[]>]
 [-PreferHTTPS] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5676d-107">-</span><span class="sxs-lookup"><span data-stu-id="5676d-107">ICMP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-IcmpProtocol] [-DisableTraceRoute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5676d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5676d-108">DESCRIPTION</span></span>
<span data-ttu-id="5676d-109">Командлет New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject создает конфигурацию протокола, используемую для оценки тестов по протоколу TCP, HTTP или ICMP.</span><span class="sxs-lookup"><span data-stu-id="5676d-109">The New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject cmdlet creates protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="5676d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5676d-110">EXAMPLES</span></span>

### <span data-ttu-id="5676d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5676d-111">Example 1</span></span>
```powershell
PS C:\>$TcpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -TcpProtocol -Port 80 -DisableTraceRoute $false
```

<span data-ttu-id="5676d-112">Порт: 80 DisableTraceRoute: ложь</span><span class="sxs-lookup"><span data-stu-id="5676d-112">Port              : 80 DisableTraceRoute : False</span></span>

## <span data-ttu-id="5676d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5676d-113">PARAMETERS</span></span>

### <span data-ttu-id="5676d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5676d-114">-DefaultProfile</span></span>
<span data-ttu-id="5676d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5676d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5676d-116">-DisableTraceRoute</span><span class="sxs-lookup"><span data-stu-id="5676d-116">-DisableTraceRoute</span></span>
<span data-ttu-id="5676d-117">Значение, указывающее, следует ли отключить оценку пути с помощью маршрута трассировки.</span><span class="sxs-lookup"><span data-stu-id="5676d-117">Value indicating whether path evaluation with trace route should be disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP, ICMP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5676d-118">-HttpProtocol</span><span class="sxs-lookup"><span data-stu-id="5676d-118">-HttpProtocol</span></span>
<span data-ttu-id="5676d-119">Коммутатор протокола HTTP</span><span class="sxs-lookup"><span data-stu-id="5676d-119">HTTP protocol switch</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5676d-120">-IcmpProtocol</span><span class="sxs-lookup"><span data-stu-id="5676d-120">-IcmpProtocol</span></span>
<span data-ttu-id="5676d-121">Переключатель протокола ICMP.</span><span class="sxs-lookup"><span data-stu-id="5676d-121">ICMP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ICMP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5676d-122">-Method</span><span class="sxs-lookup"><span data-stu-id="5676d-122">-Method</span></span>
<span data-ttu-id="5676d-123">Используемый HTTP-метод.</span><span class="sxs-lookup"><span data-stu-id="5676d-123">The HTTP method to use.</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5676d-124">-Path</span><span class="sxs-lookup"><span data-stu-id="5676d-124">-Path</span></span>
<span data-ttu-id="5676d-125">Компонент пути универсального кода ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="5676d-125">The path component of the URI.</span></span> <span data-ttu-id="5676d-126">Например, \" /Dir1/Dir2 \" .</span><span class="sxs-lookup"><span data-stu-id="5676d-126">For instance, \"/dir1/dir2\".</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5676d-127">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="5676d-127">-Port</span></span>
<span data-ttu-id="5676d-128">Порт, к которому нужно подключиться.</span><span class="sxs-lookup"><span data-stu-id="5676d-128">The port to connect to.</span></span>

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5676d-129">-PreferHTTPS</span><span class="sxs-lookup"><span data-stu-id="5676d-129">-PreferHTTPS</span></span>
<span data-ttu-id="5676d-130">Значение, указывающее, является ли протокол HTTPS предпочтительнее HTTP в случае, если выбор не является явным.</span><span class="sxs-lookup"><span data-stu-id="5676d-130">Value indicating whether HTTPS is preferred over HTTP in cases where the choice is not explicit.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5676d-131">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="5676d-131">-RequestHeader</span></span>
<span data-ttu-id="5676d-132">Заголовки HTTP для передачи с запросом.</span><span class="sxs-lookup"><span data-stu-id="5676d-132">The HTTP headers to transmit with the request.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5676d-133">-TcpProtocol</span><span class="sxs-lookup"><span data-stu-id="5676d-133">-TcpProtocol</span></span>
<span data-ttu-id="5676d-134">Переключатель протоколов TCP.</span><span class="sxs-lookup"><span data-stu-id="5676d-134">TCP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5676d-135">-ValidStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="5676d-135">-ValidStatusCodeRange</span></span>
<span data-ttu-id="5676d-136">Коды состояния HTTP для успешного рассмотрения.</span><span class="sxs-lookup"><span data-stu-id="5676d-136">HTTP status codes to consider successful.</span></span> <span data-ttu-id="5676d-137">Например, \" 2xx, 301 — 304418 \" .</span><span class="sxs-lookup"><span data-stu-id="5676d-137">For instance, \"2xx,301-304,418\".</span></span>

```yaml
Type: System.String[]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5676d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5676d-138">CommonParameters</span></span>
<span data-ttu-id="5676d-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5676d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5676d-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5676d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5676d-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5676d-141">INPUTS</span></span>

### <span data-ttu-id="5676d-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="5676d-142">None</span></span>

## <span data-ttu-id="5676d-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5676d-143">OUTPUTS</span></span>

### <span data-ttu-id="5676d-144">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorTcpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5676d-144">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorTcpConfiguration</span></span>

### <span data-ttu-id="5676d-145">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorHttpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5676d-145">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorHttpConfiguration</span></span>

### <span data-ttu-id="5676d-146">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorIcmpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5676d-146">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorIcmpConfiguration</span></span>

## <span data-ttu-id="5676d-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="5676d-147">NOTES</span></span>

## <span data-ttu-id="5676d-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5676d-148">RELATED LINKS</span></span>
