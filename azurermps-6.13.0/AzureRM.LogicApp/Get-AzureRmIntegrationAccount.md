---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
ms.openlocfilehash: d20a5db2a212ac23636fb8415586f764502c14b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734376"
---
# <span data-ttu-id="80274-101">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="80274-101">Get-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="80274-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80274-102">SYNOPSIS</span></span>
<span data-ttu-id="80274-103">Возвращает учетные записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="80274-103">Gets integration accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80274-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80274-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80274-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80274-105">DESCRIPTION</span></span>
<span data-ttu-id="80274-106">Командлет **Get-AzureRmIntegrationAccount** получает учетные записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80274-106">The **Get-AzureRmIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="80274-107">Укажите имя учетной записи интеграции и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80274-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="80274-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="80274-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="80274-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="80274-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="80274-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="80274-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="80274-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="80274-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="80274-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80274-112">EXAMPLES</span></span>

### <span data-ttu-id="80274-113">Пример 1: получение учетной записи интеграции по имени</span><span class="sxs-lookup"><span data-stu-id="80274-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="80274-114">Эта команда получает учетную запись интеграции с именем IntegrationAccount31 из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80274-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="80274-115">Пример 2: получение учетных записей интеграции в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="80274-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="80274-116">Эта команда получает учетные записи интеграции из группы ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="80274-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="80274-117">Пример 3: получение всех учетных записей интеграции</span><span class="sxs-lookup"><span data-stu-id="80274-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="80274-118">Эта команда получает все учетные записи интеграции в вашей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="80274-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="80274-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80274-119">PARAMETERS</span></span>

### <span data-ttu-id="80274-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80274-120">-DefaultProfile</span></span>
<span data-ttu-id="80274-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="80274-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80274-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="80274-122">-Name</span></span>
<span data-ttu-id="80274-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="80274-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="80274-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80274-124">-ResourceGroupName</span></span>
<span data-ttu-id="80274-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80274-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="80274-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80274-126">CommonParameters</span></span>
<span data-ttu-id="80274-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80274-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80274-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80274-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80274-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80274-129">INPUTS</span></span>

### <span data-ttu-id="80274-130">System. String</span><span class="sxs-lookup"><span data-stu-id="80274-130">System.String</span></span>

## <span data-ttu-id="80274-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80274-131">OUTPUTS</span></span>

### <span data-ttu-id="80274-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="80274-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="80274-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="80274-133">NOTES</span></span>

## <span data-ttu-id="80274-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80274-134">RELATED LINKS</span></span>

[<span data-ttu-id="80274-135">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="80274-135">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="80274-136">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="80274-136">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="80274-137">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="80274-137">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="80274-138">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="80274-138">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


