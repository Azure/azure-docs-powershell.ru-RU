---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: b13e7b63994f71f51f321428472169aea52e92f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244499"
---
# <span data-ttu-id="a55b2-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="a55b2-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="a55b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a55b2-102">SYNOPSIS</span></span>
<span data-ttu-id="a55b2-103">Возвращает учетные записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a55b2-103">Gets integration accounts.</span></span>

## <span data-ttu-id="a55b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a55b2-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a55b2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a55b2-105">DESCRIPTION</span></span>
<span data-ttu-id="a55b2-106">Командлет **Get-AzIntegrationAccount** получает учетные записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a55b2-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="a55b2-107">Укажите имя учетной записи интеграции и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a55b2-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="a55b2-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="a55b2-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a55b2-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="a55b2-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a55b2-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="a55b2-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a55b2-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="a55b2-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a55b2-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a55b2-112">EXAMPLES</span></span>

### <span data-ttu-id="a55b2-113">Пример 1: получение учетной записи интеграции по имени</span><span class="sxs-lookup"><span data-stu-id="a55b2-113">Example 1: Get an integration account by name</span></span>
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

<span data-ttu-id="a55b2-114">Эта команда получает учетную запись интеграции с именем IntegrationAccount31 из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a55b2-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="a55b2-115">Пример 2: получение учетных записей интеграции в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="a55b2-115">Example 2: Get integration accounts in a resource group</span></span>
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

<span data-ttu-id="a55b2-116">Эта команда получает учетные записи интеграции из группы ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a55b2-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="a55b2-117">Пример 3: получение всех учетных записей интеграции</span><span class="sxs-lookup"><span data-stu-id="a55b2-117">Example 3: Get all integration accounts</span></span>
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

<span data-ttu-id="a55b2-118">Эта команда получает все учетные записи интеграции в вашей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="a55b2-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="a55b2-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a55b2-119">PARAMETERS</span></span>

### <span data-ttu-id="a55b2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a55b2-120">-DefaultProfile</span></span>
<span data-ttu-id="a55b2-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a55b2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a55b2-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a55b2-122">-Name</span></span>
<span data-ttu-id="a55b2-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a55b2-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="a55b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a55b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="a55b2-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a55b2-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a55b2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a55b2-126">CommonParameters</span></span>
<span data-ttu-id="a55b2-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a55b2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a55b2-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a55b2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a55b2-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a55b2-129">INPUTS</span></span>

### <span data-ttu-id="a55b2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a55b2-130">System.String</span></span>

## <span data-ttu-id="a55b2-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a55b2-131">OUTPUTS</span></span>

### <span data-ttu-id="a55b2-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="a55b2-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="a55b2-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a55b2-133">NOTES</span></span>

## <span data-ttu-id="a55b2-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a55b2-134">RELATED LINKS</span></span>

[<span data-ttu-id="a55b2-135">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="a55b2-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="a55b2-136">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="a55b2-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="a55b2-137">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="a55b2-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="a55b2-138">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="a55b2-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


