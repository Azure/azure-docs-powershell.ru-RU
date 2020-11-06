---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: c34146079b419bceabfec1a2b9deb67c8eec658f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559720"
---
# <span data-ttu-id="93374-101">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="93374-101">Get-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="93374-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93374-102">SYNOPSIS</span></span>
<span data-ttu-id="93374-103">Получает схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="93374-103">Gets integration account schemas.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93374-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93374-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93374-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93374-105">DESCRIPTION</span></span>
<span data-ttu-id="93374-106">Командлет **Get-AzureRmIntegrationAccountSchema** получает схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="93374-106">The **Get-AzureRmIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="93374-107">Указание имени учетной записи интеграции, имени группы ресурсов и имени схемы.</span><span class="sxs-lookup"><span data-stu-id="93374-107">Specifying the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="93374-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="93374-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="93374-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="93374-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="93374-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="93374-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="93374-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="93374-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="93374-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93374-112">EXAMPLES</span></span>

### <span data-ttu-id="93374-113">Пример 1: получение схемы учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="93374-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
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

<span data-ttu-id="93374-114">Эта команда получает схему учетной записи интеграции с именем IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="93374-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="93374-115">Пример 2: получение схем учетной записи интеграции для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="93374-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="93374-116">Эта команда получает схемы учетной записи интеграции для группы ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="93374-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="93374-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93374-117">PARAMETERS</span></span>

### <span data-ttu-id="93374-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="93374-118">-Name</span></span>
<span data-ttu-id="93374-119">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="93374-119">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="93374-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93374-120">-ResourceGroupName</span></span>
<span data-ttu-id="93374-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93374-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="93374-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="93374-122">-SchemaName</span></span>
<span data-ttu-id="93374-123">Указывает имя схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="93374-123">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="93374-124">Указывает имя схемы.</span><span class="sxs-lookup"><span data-stu-id="93374-124">Specifies the name of a schema.</span></span>
<span data-ttu-id="93374-125">.</span><span class="sxs-lookup"><span data-stu-id="93374-125">.</span></span>

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

### <span data-ttu-id="93374-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93374-126">-DefaultProfile</span></span>
<span data-ttu-id="93374-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93374-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93374-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93374-128">CommonParameters</span></span>
<span data-ttu-id="93374-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93374-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93374-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93374-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93374-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93374-131">INPUTS</span></span>

## <span data-ttu-id="93374-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93374-132">OUTPUTS</span></span>

### <span data-ttu-id="93374-133">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="93374-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="93374-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="93374-134">NOTES</span></span>

## <span data-ttu-id="93374-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93374-135">RELATED LINKS</span></span>

[<span data-ttu-id="93374-136">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="93374-136">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="93374-137">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="93374-137">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="93374-138">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="93374-138">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


