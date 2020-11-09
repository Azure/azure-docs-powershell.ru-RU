---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8fb1f76b32332c7679ef59f50123072311de86fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248362"
---
# <span data-ttu-id="332c5-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="332c5-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="332c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="332c5-102">SYNOPSIS</span></span>
<span data-ttu-id="332c5-103">Получить Поддерживаемые серверные переменные и доступные заголовки запросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="332c5-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="332c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="332c5-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="332c5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="332c5-105">DESCRIPTION</span></span>
<span data-ttu-id="332c5-106">Командлет **Get-AzApplicationGatewayAvailableServerVariableAndHeader** возвращает Поддерживаемые серверные переменные и доступные заголовки запросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="332c5-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="332c5-107">Параметры можно использовать для получения списков переменных или заголовков.</span><span class="sxs-lookup"><span data-stu-id="332c5-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="332c5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="332c5-108">EXAMPLES</span></span>

### <span data-ttu-id="332c5-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="332c5-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="332c5-110">Эти команды возвращают все доступные переменные сервера.</span><span class="sxs-lookup"><span data-stu-id="332c5-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="332c5-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="332c5-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="332c5-112">Эти команды возвращают все доступные заголовки запроса.</span><span class="sxs-lookup"><span data-stu-id="332c5-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="332c5-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="332c5-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="332c5-114">Эти команды возвращают все доступные заголовки ответов.</span><span class="sxs-lookup"><span data-stu-id="332c5-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="332c5-115">Пример 4</span><span class="sxs-lookup"><span data-stu-id="332c5-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="332c5-116">Эти команды возвращают все доступные серверные переменные, заголовки запросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="332c5-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="332c5-117">Пример 5</span><span class="sxs-lookup"><span data-stu-id="332c5-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="332c5-118">Эти команды возвращают все доступные серверные переменные, заголовки запросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="332c5-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="332c5-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="332c5-119">PARAMETERS</span></span>

### <span data-ttu-id="332c5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="332c5-120">-DefaultProfile</span></span>
<span data-ttu-id="332c5-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="332c5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="332c5-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="332c5-122">-RequestHeader</span></span>
<span data-ttu-id="332c5-123">Заголовков запросов на доступ к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="332c5-123">Application Gateway available request headers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="332c5-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="332c5-124">-ResponseHeader</span></span>
<span data-ttu-id="332c5-125">Заголовки ответов для доступных шлюзов приложений.</span><span class="sxs-lookup"><span data-stu-id="332c5-125">Application Gateway available response headers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="332c5-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="332c5-126">-ServerVariable</span></span>
<span data-ttu-id="332c5-127">Доступные переменные сервера для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="332c5-127">Application Gateway available server variables.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="332c5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="332c5-128">CommonParameters</span></span>
<span data-ttu-id="332c5-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="332c5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="332c5-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="332c5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="332c5-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="332c5-131">INPUTS</span></span>

### <span data-ttu-id="332c5-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="332c5-132">None</span></span>

## <span data-ttu-id="332c5-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="332c5-133">OUTPUTS</span></span>

### <span data-ttu-id="332c5-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="332c5-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="332c5-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="332c5-135">NOTES</span></span>
<span data-ttu-id="332c5-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** — псевдоним для командлета **Get-AzApplicationGatewayAvailableServerVariableAndHeader** .</span><span class="sxs-lookup"><span data-stu-id="332c5-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="332c5-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="332c5-137">RELATED LINKS</span></span>