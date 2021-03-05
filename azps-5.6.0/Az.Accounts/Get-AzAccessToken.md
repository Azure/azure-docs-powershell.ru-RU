---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 5fcd81dcfc69f020a4e17e0858abfca0edaba405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973027"
---
# <span data-ttu-id="49245-101">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="49245-101">Get-AzAccessToken</span></span>

## <span data-ttu-id="49245-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49245-102">SYNOPSIS</span></span>
<span data-ttu-id="49245-103">Получить необработанные маркеры доступа.</span><span class="sxs-lookup"><span data-stu-id="49245-103">Get raw access token.</span></span> <span data-ttu-id="49245-104">При использовании ресурса ResourceUrl убедитесь, что значение соответствует текущей среде Azure.</span><span class="sxs-lookup"><span data-stu-id="49245-104">When using -ResourceUrl, please make sure the value does match current Azure environment.</span></span> <span data-ttu-id="49245-105">Вы можете ссылаться на значение `(Get-AzContext).Environment` .</span><span class="sxs-lookup"><span data-stu-id="49245-105">You may refer to the value of `(Get-AzContext).Environment`.</span></span>

## <span data-ttu-id="49245-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="49245-106">SYNTAX</span></span>

### <span data-ttu-id="49245-107">KnownResourceTypeName (Default)</span><span class="sxs-lookup"><span data-stu-id="49245-107">KnownResourceTypeName (Default)</span></span>
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49245-108">ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="49245-108">ResourceUrl</span></span>
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49245-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49245-109">DESCRIPTION</span></span>
<span data-ttu-id="49245-110">Получить маркер доступа</span><span class="sxs-lookup"><span data-stu-id="49245-110">Get access token</span></span>

## <span data-ttu-id="49245-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="49245-111">EXAMPLES</span></span>

### <span data-ttu-id="49245-112">Пример 1. Получить необработанные маркеры доступа для ARM конечной точки</span><span class="sxs-lookup"><span data-stu-id="49245-112">Example 1 Get raw access token for ARM endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken
```

<span data-ttu-id="49245-113">Получить маркер доступа конечной точки "Ресурс" для текущей учетной записи</span><span class="sxs-lookup"><span data-stu-id="49245-113">Get access token of ResourceManager endpoint for current account</span></span>

### <span data-ttu-id="49245-114">Пример 2. Получить необработанные маркеры доступа для конечной точки AAD Graph</span><span class="sxs-lookup"><span data-stu-id="49245-114">Example 2 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

<span data-ttu-id="49245-115">Получить маркер доступа конечной точки AAD Graph для текущей учетной записи</span><span class="sxs-lookup"><span data-stu-id="49245-115">Get access token of AAD graph endpoint for current account</span></span>

### <span data-ttu-id="49245-116">Пример 3. Получить необработанные маркеры доступа для конечной точки AAD Graph</span><span class="sxs-lookup"><span data-stu-id="49245-116">Example 3 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

<span data-ttu-id="49245-117">Получить маркер доступа конечной точки AAD Graph для текущей учетной записи</span><span class="sxs-lookup"><span data-stu-id="49245-117">Get access token of AAD graph endpoint for current account</span></span>

## <span data-ttu-id="49245-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49245-118">PARAMETERS</span></span>

### <span data-ttu-id="49245-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49245-119">-DefaultProfile</span></span>
<span data-ttu-id="49245-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49245-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49245-121">-ResourceTypeName</span><span class="sxs-lookup"><span data-stu-id="49245-121">-ResourceTypeName</span></span>
<span data-ttu-id="49245-122">Необязательное имя типа повторного сведения, поддерживаемые значения: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span><span class="sxs-lookup"><span data-stu-id="49245-122">Optional resouce type name, supported values: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span></span> <span data-ttu-id="49245-123">Значение по умолчанию — Arm, если не указано.</span><span class="sxs-lookup"><span data-stu-id="49245-123">Default value is Arm if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49245-124">-ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="49245-124">-ResourceUrl</span></span>
<span data-ttu-id="49245-125">URL-адрес ресурса, для который запрашивается токен, например ' http://graph.windows.net/ .</span><span class="sxs-lookup"><span data-stu-id="49245-125">Resource url for that you're requesting token, e.g. 'http://graph.windows.net/'.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49245-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="49245-126">-TenantId</span></span>
<span data-ttu-id="49245-127">Необязательный ИД клиента. Используйте стандартный контекст с ид клиента, если он не указан.</span><span class="sxs-lookup"><span data-stu-id="49245-127">Optional Tenant Id. Use tenant id of default context if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49245-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49245-128">CommonParameters</span></span>
<span data-ttu-id="49245-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49245-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49245-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49245-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49245-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49245-131">INPUTS</span></span>

### <span data-ttu-id="49245-132">Нет</span><span class="sxs-lookup"><span data-stu-id="49245-132">None</span></span>

## <span data-ttu-id="49245-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49245-133">OUTPUTS</span></span>

### <span data-ttu-id="49245-134">System.String</span><span class="sxs-lookup"><span data-stu-id="49245-134">System.String</span></span>

## <span data-ttu-id="49245-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="49245-135">NOTES</span></span>

## <span data-ttu-id="49245-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49245-136">RELATED LINKS</span></span>
