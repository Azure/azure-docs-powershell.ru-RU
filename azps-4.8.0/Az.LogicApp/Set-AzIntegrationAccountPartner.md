---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
ms.openlocfilehash: edd50a72ed0614cf7c71dfbde9f487e8fe632d85
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079573"
---
# <span data-ttu-id="fc601-101">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="fc601-101">Set-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="fc601-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc601-102">SYNOPSIS</span></span>
<span data-ttu-id="fc601-103">Изменение партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="fc601-103">Modifies an integration account partner.</span></span>

## <span data-ttu-id="fc601-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc601-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc601-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc601-105">DESCRIPTION</span></span>
<span data-ttu-id="fc601-106">Командлет **Set-AzIntegrationAccountPartner** изменяет партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="fc601-106">The **Set-AzIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="fc601-107">Этот командлет возвращает объект, представляющий партнера по учетным записям интеграции.</span><span class="sxs-lookup"><span data-stu-id="fc601-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="fc601-108">Укажите имя учетной записи интеграции, имя группы ресурсов и имя партнера.</span><span class="sxs-lookup"><span data-stu-id="fc601-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="fc601-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="fc601-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fc601-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="fc601-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fc601-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="fc601-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fc601-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="fc601-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="fc601-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc601-113">EXAMPLES</span></span>

### <span data-ttu-id="fc601-114">Пример 1: изменение партнера учетной записи для интеграции</span><span class="sxs-lookup"><span data-stu-id="fc601-114">Example 1: Modify an integration account partner</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="fc601-115">Эта команда изменяет партнера учетной записи интеграции с именем IntegrationAccountPartner22 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc601-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

### <span data-ttu-id="fc601-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fc601-116">Example 2</span></span>

<span data-ttu-id="fc601-117">Изменение партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="fc601-117">Modifies an integration account partner.</span></span> <span data-ttu-id="fc601-118">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="fc601-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountPartner -BusinessIdentities <Object> -Metadata <Object> -Name 'IntegrationAccount31' -PartnerName 'IntegrationAccountPartner22' -PartnerType B2B -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="fc601-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc601-119">PARAMETERS</span></span>

### <span data-ttu-id="fc601-120">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="fc601-120">-BusinessIdentities</span></span>
<span data-ttu-id="fc601-121">Указывает бизнес-идентификаторы для партнера по учетным записям интеграции.</span><span class="sxs-lookup"><span data-stu-id="fc601-121">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="fc601-122">Укажите хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="fc601-122">Specify a hash table.</span></span>

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

### <span data-ttu-id="fc601-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc601-123">-DefaultProfile</span></span>
<span data-ttu-id="fc601-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fc601-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc601-125">-Force</span><span class="sxs-lookup"><span data-stu-id="fc601-125">-Force</span></span>
<span data-ttu-id="fc601-126">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc601-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fc601-127">-Metadata</span><span class="sxs-lookup"><span data-stu-id="fc601-127">-Metadata</span></span>
<span data-ttu-id="fc601-128">Указывает объект метаданных для партнера.</span><span class="sxs-lookup"><span data-stu-id="fc601-128">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="fc601-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fc601-129">-Name</span></span>
<span data-ttu-id="fc601-130">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="fc601-130">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="fc601-131">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="fc601-131">-PartnerName</span></span>
<span data-ttu-id="fc601-132">Указывает имя партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="fc601-132">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="fc601-133">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="fc601-133">-PartnerType</span></span>
<span data-ttu-id="fc601-134">Указывает тип учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="fc601-134">Specifies the type of the integration account.</span></span>
<span data-ttu-id="fc601-135">Этот параметр поддерживает тип B2B.</span><span class="sxs-lookup"><span data-stu-id="fc601-135">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="fc601-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc601-136">-ResourceGroupName</span></span>
<span data-ttu-id="fc601-137">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc601-137">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fc601-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc601-138">-Confirm</span></span>
<span data-ttu-id="fc601-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fc601-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc601-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc601-140">-WhatIf</span></span>
<span data-ttu-id="fc601-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fc601-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc601-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fc601-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc601-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc601-143">CommonParameters</span></span>
<span data-ttu-id="fc601-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc601-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc601-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc601-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc601-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc601-146">INPUTS</span></span>

### <span data-ttu-id="fc601-147">System. String</span><span class="sxs-lookup"><span data-stu-id="fc601-147">System.String</span></span>

## <span data-ttu-id="fc601-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc601-148">OUTPUTS</span></span>

### <span data-ttu-id="fc601-149">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="fc601-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="fc601-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc601-150">NOTES</span></span>

## <span data-ttu-id="fc601-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc601-151">RELATED LINKS</span></span>

[<span data-ttu-id="fc601-152">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="fc601-152">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="fc601-153">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="fc601-153">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="fc601-154">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="fc601-154">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)


