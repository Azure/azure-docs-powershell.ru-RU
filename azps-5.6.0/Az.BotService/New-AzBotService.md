---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/new-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
ms.openlocfilehash: 11f3124c98e84dcaec40c3b8ecd9b8831b572617
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009299"
---
# <span data-ttu-id="50138-101">New-AzBotService</span><span class="sxs-lookup"><span data-stu-id="50138-101">New-AzBotService</span></span>

## <span data-ttu-id="50138-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50138-102">SYNOPSIS</span></span>
<span data-ttu-id="50138-103">Возвращает ботслужба, заданную параметрами.</span><span class="sxs-lookup"><span data-stu-id="50138-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="50138-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="50138-104">SYNTAX</span></span>

### <span data-ttu-id="50138-105">Регистрация (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="50138-105">Registration (Default)</span></span>
```
New-AzBotService -ApplicationId <String> -Location <String> [-BotTemplateType <String>]
 [-Description <String>] [-DisplayName <String>] [-Endpoint <String>] [-Language <String>] [-Name <String>]
 [-Registration] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="50138-106">WebApp</span><span class="sxs-lookup"><span data-stu-id="50138-106">WebApp</span></span>
```
New-AzBotService -ApplicationId <String> -ApplicationSecret <SecureString> -Location <String>
 [-BotTemplateType <String>] [-Description <String>] [-ExistingServerFarmId <String>] [-Language <String>]
 [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Webapp] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="50138-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50138-107">DESCRIPTION</span></span>
<span data-ttu-id="50138-108">Возвращает ботслужба, заданную параметрами.</span><span class="sxs-lookup"><span data-stu-id="50138-108">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="50138-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="50138-109">EXAMPLES</span></span>

### <span data-ttu-id="50138-110">Пример 1. Создание нового бота</span><span class="sxs-lookup"><span data-stu-id="50138-110">Example 1: Create a new bot</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-bot1 -ApplicationId "af5fce4d-ee68-4b25-be09-f3222582e133"-Location eastus -Sku F0 -Description "123134" -Registration

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="50138-111">Создание нового бота по resourceGroupName и ApplicationId</span><span class="sxs-lookup"><span data-stu-id="50138-111">Create a new Bot by ResourceGroupName and ApplicationId</span></span>

### <span data-ttu-id="50138-112">Пример 2. Создание веб-приложения</span><span class="sxs-lookup"><span data-stu-id="50138-112">Example 2: Create a new Web App</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-apptest14 -ApplicationId "b1ab1727-0465-4255-a1bb-976210af972c" -Location eastus -Sku F0 -Description "123134" -Webapp

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest14 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="50138-113">Создание веб-приложения по resourceGroupName и ApplicationId</span><span class="sxs-lookup"><span data-stu-id="50138-113">Create a new Web App by ResourceGroupName and ApplicationId</span></span>

## <span data-ttu-id="50138-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50138-114">PARAMETERS</span></span>

### <span data-ttu-id="50138-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="50138-115">-ApplicationId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50138-116">-ApplicationSecret</span><span class="sxs-lookup"><span data-stu-id="50138-116">-ApplicationSecret</span></span>


```yaml
Type: System.Security.SecureString
Parameter Sets: WebApp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50138-117">-BotTemplateType</span><span class="sxs-lookup"><span data-stu-id="50138-117">-BotTemplateType</span></span>


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

### <span data-ttu-id="50138-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50138-118">-DefaultProfile</span></span>
<span data-ttu-id="50138-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50138-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50138-120">-Description</span><span class="sxs-lookup"><span data-stu-id="50138-120">-Description</span></span>


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

### <span data-ttu-id="50138-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="50138-121">-DisplayName</span></span>


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50138-122">-Конечная точка</span><span class="sxs-lookup"><span data-stu-id="50138-122">-Endpoint</span></span>


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50138-123">-ExistingServerFarmId</span><span class="sxs-lookup"><span data-stu-id="50138-123">-ExistingServerFarmId</span></span>


```yaml
Type: System.String
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50138-124">-Language</span><span class="sxs-lookup"><span data-stu-id="50138-124">-Language</span></span>


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

### <span data-ttu-id="50138-125">-Location</span><span class="sxs-lookup"><span data-stu-id="50138-125">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50138-126">-Name</span><span class="sxs-lookup"><span data-stu-id="50138-126">-Name</span></span>
<span data-ttu-id="50138-127">Имя ресурса-бота.</span><span class="sxs-lookup"><span data-stu-id="50138-127">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50138-128">-Registration</span><span class="sxs-lookup"><span data-stu-id="50138-128">-Registration</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50138-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50138-129">-ResourceGroupName</span></span>
<span data-ttu-id="50138-130">Имя группы ресурсов бота в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="50138-130">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="50138-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="50138-131">-Sku</span></span>
<span data-ttu-id="50138-132">Имя SKU</span><span class="sxs-lookup"><span data-stu-id="50138-132">The sku name</span></span>

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

### <span data-ttu-id="50138-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50138-133">-SubscriptionId</span></span>
<span data-ttu-id="50138-134">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="50138-134">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50138-135">-Webapp</span><span class="sxs-lookup"><span data-stu-id="50138-135">-Webapp</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50138-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50138-136">CommonParameters</span></span>
<span data-ttu-id="50138-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50138-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50138-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50138-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50138-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50138-139">INPUTS</span></span>

## <span data-ttu-id="50138-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50138-140">OUTPUTS</span></span>

### <span data-ttu-id="50138-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="50138-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="50138-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="50138-142">NOTES</span></span>

<span data-ttu-id="50138-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="50138-143">ALIASES</span></span>

## <span data-ttu-id="50138-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50138-144">RELATED LINKS</span></span>

