---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: b13e7b63994f71f51f321428472169aea52e92f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226388"
---
# <span data-ttu-id="537df-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="537df-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="537df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="537df-102">SYNOPSIS</span></span>
<span data-ttu-id="537df-103">Получает учетные записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="537df-103">Gets integration accounts.</span></span>

## <span data-ttu-id="537df-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="537df-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="537df-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="537df-105">DESCRIPTION</span></span>
<span data-ttu-id="537df-106">С **его учетной** записью можно получить учетные записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="537df-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="537df-107">Укажите имя учетной записи интеграции и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="537df-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="537df-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="537df-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="537df-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="537df-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="537df-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="537df-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="537df-111">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="537df-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="537df-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="537df-112">EXAMPLES</span></span>

### <span data-ttu-id="537df-113">Пример 1. Получить учетную запись интеграции по имени</span><span class="sxs-lookup"><span data-stu-id="537df-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="537df-114">Эта команда получает учетную запись интеграции IntegrationAccount31 из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="537df-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="537df-115">Пример 2. Интеграция учетных записей в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="537df-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="537df-116">Эта команда получает учетные записи интеграции из группы ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="537df-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="537df-117">Пример 3. Получить все учетные записи интеграции</span><span class="sxs-lookup"><span data-stu-id="537df-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="537df-118">Эта команда получает все учетные записи интеграции в вашей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="537df-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="537df-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="537df-119">PARAMETERS</span></span>

### <span data-ttu-id="537df-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="537df-120">-DefaultProfile</span></span>
<span data-ttu-id="537df-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="537df-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="537df-122">-Name</span><span class="sxs-lookup"><span data-stu-id="537df-122">-Name</span></span>
<span data-ttu-id="537df-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="537df-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="537df-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="537df-124">-ResourceGroupName</span></span>
<span data-ttu-id="537df-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="537df-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="537df-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="537df-126">CommonParameters</span></span>
<span data-ttu-id="537df-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="537df-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="537df-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="537df-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="537df-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="537df-129">INPUTS</span></span>

### <span data-ttu-id="537df-130">System.String</span><span class="sxs-lookup"><span data-stu-id="537df-130">System.String</span></span>

## <span data-ttu-id="537df-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="537df-131">OUTPUTS</span></span>

### <span data-ttu-id="537df-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="537df-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="537df-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="537df-133">NOTES</span></span>

## <span data-ttu-id="537df-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="537df-134">RELATED LINKS</span></span>

[<span data-ttu-id="537df-135">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="537df-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="537df-136">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="537df-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="537df-137">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="537df-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="537df-138">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="537df-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


