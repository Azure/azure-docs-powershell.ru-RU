---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
ms.openlocfilehash: 5961741be40e52a705395d34d5b731715dff27a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960568"
---
# <span data-ttu-id="94d21-101">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="94d21-101">Get-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="94d21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94d21-102">SYNOPSIS</span></span>
<span data-ttu-id="94d21-103">Интеграция схем учетных записей.</span><span class="sxs-lookup"><span data-stu-id="94d21-103">Gets integration account schemas.</span></span>

## <span data-ttu-id="94d21-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94d21-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94d21-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94d21-105">DESCRIPTION</span></span>
<span data-ttu-id="94d21-106">**Cmdlet Get-AzIntegrationAccountSchema** возвращает схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="94d21-106">The **Get-AzIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="94d21-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя схемы.</span><span class="sxs-lookup"><span data-stu-id="94d21-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="94d21-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="94d21-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="94d21-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="94d21-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="94d21-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="94d21-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="94d21-111">Если не задан параметр обязательного шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="94d21-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="94d21-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94d21-112">EXAMPLES</span></span>

### <span data-ttu-id="94d21-113">Пример 1. Получить схему интеграции с учетной записью</span><span class="sxs-lookup"><span data-stu-id="94d21-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="94d21-114">Эта команда получает схему учетной записи интеграции IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="94d21-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="94d21-115">Пример 2. Интеграция схем учетных записей для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="94d21-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="94d21-116">Эта команда получает схемы учетных записей интеграции для группы ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="94d21-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="94d21-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94d21-117">PARAMETERS</span></span>

### <span data-ttu-id="94d21-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d21-118">-DefaultProfile</span></span>
<span data-ttu-id="94d21-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="94d21-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94d21-120">-Name</span><span class="sxs-lookup"><span data-stu-id="94d21-120">-Name</span></span>
<span data-ttu-id="94d21-121">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="94d21-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="94d21-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94d21-122">-ResourceGroupName</span></span>
<span data-ttu-id="94d21-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94d21-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="94d21-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="94d21-124">-SchemaName</span></span>
<span data-ttu-id="94d21-125">Имя схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="94d21-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="94d21-126">Указывает имя схемы.</span><span class="sxs-lookup"><span data-stu-id="94d21-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="94d21-127">.</span><span class="sxs-lookup"><span data-stu-id="94d21-127">.</span></span>

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

### <span data-ttu-id="94d21-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d21-128">CommonParameters</span></span>
<span data-ttu-id="94d21-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94d21-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d21-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94d21-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d21-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94d21-131">INPUTS</span></span>

### <span data-ttu-id="94d21-132">System.String</span><span class="sxs-lookup"><span data-stu-id="94d21-132">System.String</span></span>

## <span data-ttu-id="94d21-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94d21-133">OUTPUTS</span></span>

### <span data-ttu-id="94d21-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="94d21-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="94d21-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94d21-135">NOTES</span></span>

## <span data-ttu-id="94d21-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94d21-136">RELATED LINKS</span></span>

[<span data-ttu-id="94d21-137">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="94d21-137">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="94d21-138">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="94d21-138">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="94d21-139">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="94d21-139">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


