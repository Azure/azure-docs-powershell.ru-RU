---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
ms.openlocfilehash: ed85c1fea8bd338b3dd4f2a9e82ee5aac3f3b52b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518262"
---
# <span data-ttu-id="83e88-101">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="83e88-101">Get-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="83e88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83e88-102">SYNOPSIS</span></span>
<span data-ttu-id="83e88-103">Интеграция схем учетных записей.</span><span class="sxs-lookup"><span data-stu-id="83e88-103">Gets integration account schemas.</span></span>

## <span data-ttu-id="83e88-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="83e88-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83e88-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83e88-105">DESCRIPTION</span></span>
<span data-ttu-id="83e88-106">**Cmdlet Get-AzIntegrationAccountSchema** возвращает схемы учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="83e88-106">The **Get-AzIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="83e88-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя схемы.</span><span class="sxs-lookup"><span data-stu-id="83e88-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="83e88-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="83e88-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="83e88-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="83e88-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="83e88-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="83e88-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="83e88-111">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="83e88-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="83e88-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="83e88-112">EXAMPLES</span></span>

### <span data-ttu-id="83e88-113">Пример 1. Получить схему интеграции с учетной записью</span><span class="sxs-lookup"><span data-stu-id="83e88-113">Example 1: Get an integration account schema</span></span>
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

<span data-ttu-id="83e88-114">Эта команда получает схему учетной записи интеграции IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="83e88-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="83e88-115">Пример 2. Интеграция схем учетных записей для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="83e88-115">Example 2: Get integration account schemas for a resource group</span></span>
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

<span data-ttu-id="83e88-116">Эта команда получает схемы учетных записей интеграции для группы ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="83e88-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="83e88-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83e88-117">PARAMETERS</span></span>

### <span data-ttu-id="83e88-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e88-118">-DefaultProfile</span></span>
<span data-ttu-id="83e88-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="83e88-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83e88-120">-Name</span><span class="sxs-lookup"><span data-stu-id="83e88-120">-Name</span></span>
<span data-ttu-id="83e88-121">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="83e88-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="83e88-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83e88-122">-ResourceGroupName</span></span>
<span data-ttu-id="83e88-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83e88-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="83e88-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="83e88-124">-SchemaName</span></span>
<span data-ttu-id="83e88-125">Указывает имя схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="83e88-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="83e88-126">Указывает имя схемы.</span><span class="sxs-lookup"><span data-stu-id="83e88-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="83e88-127">.</span><span class="sxs-lookup"><span data-stu-id="83e88-127">.</span></span>

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

### <span data-ttu-id="83e88-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e88-128">CommonParameters</span></span>
<span data-ttu-id="83e88-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83e88-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e88-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83e88-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e88-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83e88-131">INPUTS</span></span>

### <span data-ttu-id="83e88-132">System.String</span><span class="sxs-lookup"><span data-stu-id="83e88-132">System.String</span></span>

## <span data-ttu-id="83e88-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="83e88-133">OUTPUTS</span></span>

### <span data-ttu-id="83e88-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="83e88-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="83e88-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="83e88-135">NOTES</span></span>

## <span data-ttu-id="83e88-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83e88-136">RELATED LINKS</span></span>

[<span data-ttu-id="83e88-137">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="83e88-137">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="83e88-138">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="83e88-138">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="83e88-139">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="83e88-139">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


