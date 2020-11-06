---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: f59c3e1896fd60dd70c1708a66ca8bbf360342ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568901"
---
# <span data-ttu-id="da7a9-101">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="da7a9-101">New-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="da7a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="da7a9-103">Создает партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="da7a9-103">Creates an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da7a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da7a9-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da7a9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da7a9-105">DESCRIPTION</span></span>
<span data-ttu-id="da7a9-106">Командлет **New-AzureRmIntegrationAccountPartner** создает партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="da7a9-106">The **New-AzureRmIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="da7a9-107">Этот командлет возвращает объект, представляющий партнера по учетным записям интеграции.</span><span class="sxs-lookup"><span data-stu-id="da7a9-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="da7a9-108">Укажите имя учетной записи интеграции, имя группы ресурсов, имя партнера и идентификаторы партнеров.</span><span class="sxs-lookup"><span data-stu-id="da7a9-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>
<span data-ttu-id="da7a9-109">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="da7a9-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="da7a9-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="da7a9-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="da7a9-111">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="da7a9-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="da7a9-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="da7a9-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="da7a9-113">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="da7a9-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="da7a9-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da7a9-114">EXAMPLES</span></span>

### <span data-ttu-id="da7a9-115">Пример 1: создание партнера учетной записи для интеграции</span><span class="sxs-lookup"><span data-stu-id="da7a9-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="da7a9-116">Эта команда создает партнера учетной записи интеграции с именем IntegrationAccountPartner22 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="da7a9-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="da7a9-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da7a9-117">PARAMETERS</span></span>

### <span data-ttu-id="da7a9-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="da7a9-118">-BusinessIdentities</span></span>
<span data-ttu-id="da7a9-119">Указывает бизнес-идентификаторы для партнера по учетным записям интеграции.</span><span class="sxs-lookup"><span data-stu-id="da7a9-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="da7a9-120">Укажите хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="da7a9-120">Specify a hash table.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7a9-121">-DefaultProfile</span></span>
<span data-ttu-id="da7a9-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="da7a9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da7a9-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="da7a9-123">-Metadata</span></span>
<span data-ttu-id="da7a9-124">Указывает объект метаданных для партнера.</span><span class="sxs-lookup"><span data-stu-id="da7a9-124">Specifies a metadata object for the partner.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a9-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da7a9-125">-Name</span></span>
<span data-ttu-id="da7a9-126">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="da7a9-126">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7a9-127">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="da7a9-127">-PartnerName</span></span>
<span data-ttu-id="da7a9-128">Указывает имя для партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="da7a9-128">Specifies a name for the integration account partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7a9-129">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="da7a9-129">-PartnerType</span></span>
<span data-ttu-id="da7a9-130">Указывает тип учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="da7a9-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="da7a9-131">Этот параметр поддерживает тип B2B.</span><span class="sxs-lookup"><span data-stu-id="da7a9-131">This parameter supports the type B2B.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da7a9-132">-ResourceGroupName</span></span>
<span data-ttu-id="da7a9-133">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="da7a9-133">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7a9-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da7a9-134">-Confirm</span></span>
<span data-ttu-id="da7a9-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="da7a9-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da7a9-136">-WhatIf</span></span>
<span data-ttu-id="da7a9-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="da7a9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da7a9-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="da7a9-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7a9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7a9-139">CommonParameters</span></span>
<span data-ttu-id="da7a9-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da7a9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7a9-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da7a9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7a9-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da7a9-142">INPUTS</span></span>

### <span data-ttu-id="da7a9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="da7a9-143">System.String</span></span>

## <span data-ttu-id="da7a9-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da7a9-144">OUTPUTS</span></span>

### <span data-ttu-id="da7a9-145">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="da7a9-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="da7a9-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="da7a9-146">NOTES</span></span>

## <span data-ttu-id="da7a9-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da7a9-147">RELATED LINKS</span></span>

[<span data-ttu-id="da7a9-148">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="da7a9-148">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="da7a9-149">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="da7a9-149">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="da7a9-150">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="da7a9-150">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


