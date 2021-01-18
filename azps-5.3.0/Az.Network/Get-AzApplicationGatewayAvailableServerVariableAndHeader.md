---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8fb1f76b32332c7679ef59f50123072311de86fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506545"
---
# <span data-ttu-id="a3b37-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="a3b37-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="a3b37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3b37-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b37-103">Получите поддерживаемые переменные сервера, а также доступные заглавные данные запросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="a3b37-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="a3b37-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a3b37-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="a3b37-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3b37-105">DESCRIPTION</span></span>
<span data-ttu-id="a3b37-106">Cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader** получает поддерживаемые переменные сервера, а также доступные заголовок запроса и ответа.</span><span class="sxs-lookup"><span data-stu-id="a3b37-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="a3b37-107">Параметры можно использовать для получения списков переменных или заглавных параметров.</span><span class="sxs-lookup"><span data-stu-id="a3b37-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="a3b37-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a3b37-108">EXAMPLES</span></span>

### <span data-ttu-id="a3b37-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a3b37-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="a3b37-110">Эти команды возвращают все доступные серверные переменные.</span><span class="sxs-lookup"><span data-stu-id="a3b37-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="a3b37-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a3b37-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="a3b37-112">Эти команды возвращают все доступные заглавные данные запроса.</span><span class="sxs-lookup"><span data-stu-id="a3b37-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="a3b37-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a3b37-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="a3b37-114">Эти команды возвращают все доступные заглавные ответы.</span><span class="sxs-lookup"><span data-stu-id="a3b37-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="a3b37-115">Пример 4</span><span class="sxs-lookup"><span data-stu-id="a3b37-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="a3b37-116">Эти команды возвращают все доступные серверные переменные, заглавные запросы и ответы.</span><span class="sxs-lookup"><span data-stu-id="a3b37-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="a3b37-117">Пример 5</span><span class="sxs-lookup"><span data-stu-id="a3b37-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="a3b37-118">Эти команды возвращают все доступные серверные переменные, заглавные запросы и ответы.</span><span class="sxs-lookup"><span data-stu-id="a3b37-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="a3b37-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3b37-119">PARAMETERS</span></span>

### <span data-ttu-id="a3b37-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b37-120">-DefaultProfile</span></span>
<span data-ttu-id="a3b37-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3b37-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3b37-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="a3b37-122">-RequestHeader</span></span>
<span data-ttu-id="a3b37-123">Доступные заглавные данные запроса шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a3b37-123">Application Gateway available request headers.</span></span>

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

### <span data-ttu-id="a3b37-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="a3b37-124">-ResponseHeader</span></span>
<span data-ttu-id="a3b37-125">Заглавные ответы шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a3b37-125">Application Gateway available response headers.</span></span>

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

### <span data-ttu-id="a3b37-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="a3b37-126">-ServerVariable</span></span>
<span data-ttu-id="a3b37-127">Переменные сервера, доступные для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="a3b37-127">Application Gateway available server variables.</span></span>

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

### <span data-ttu-id="a3b37-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b37-128">CommonParameters</span></span>
<span data-ttu-id="a3b37-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3b37-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b37-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3b37-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b37-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3b37-131">INPUTS</span></span>

### <span data-ttu-id="a3b37-132">Нет</span><span class="sxs-lookup"><span data-stu-id="a3b37-132">None</span></span>

## <span data-ttu-id="a3b37-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a3b37-133">OUTPUTS</span></span>

### <span data-ttu-id="a3b37-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="a3b37-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="a3b37-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a3b37-135">NOTES</span></span>
<span data-ttu-id="a3b37-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** — псевдоним для cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader.**</span><span class="sxs-lookup"><span data-stu-id="a3b37-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="a3b37-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3b37-137">RELATED LINKS</span></span>
