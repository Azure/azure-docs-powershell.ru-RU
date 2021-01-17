---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
ms.openlocfilehash: edd50a72ed0614cf7c71dfbde9f487e8fe632d85
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415572"
---
# <span data-ttu-id="abd2a-101">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="abd2a-101">Set-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="abd2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abd2a-102">SYNOPSIS</span></span>
<span data-ttu-id="abd2a-103">Изменяет партнера по интеграции с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="abd2a-103">Modifies an integration account partner.</span></span>

## <span data-ttu-id="abd2a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="abd2a-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abd2a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="abd2a-105">DESCRIPTION</span></span>
<span data-ttu-id="abd2a-106">**Cmdlet Set-AzIntegrationAccountPartner** изменяет партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="abd2a-106">The **Set-AzIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="abd2a-107">Этот cmdlet возвращает объект, который представляет партнера по учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="abd2a-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="abd2a-108">Укажите имя учетной записи интеграции, имя группы ресурсов и имя партнера.</span><span class="sxs-lookup"><span data-stu-id="abd2a-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="abd2a-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="abd2a-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="abd2a-110">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="abd2a-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="abd2a-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="abd2a-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="abd2a-112">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="abd2a-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="abd2a-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="abd2a-113">EXAMPLES</span></span>

### <span data-ttu-id="abd2a-114">Пример 1. Изменение партнера по интеграции с учетной записью</span><span class="sxs-lookup"><span data-stu-id="abd2a-114">Example 1: Modify an integration account partner</span></span>
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

<span data-ttu-id="abd2a-115">Эта команда изменит партнера по интеграции с именем IntegrationAccountPartner22 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="abd2a-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

### <span data-ttu-id="abd2a-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="abd2a-116">Example 2</span></span>

<span data-ttu-id="abd2a-117">Изменяет партнера по интеграции с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="abd2a-117">Modifies an integration account partner.</span></span> <span data-ttu-id="abd2a-118">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="abd2a-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountPartner -BusinessIdentities <Object> -Metadata <Object> -Name 'IntegrationAccount31' -PartnerName 'IntegrationAccountPartner22' -PartnerType B2B -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="abd2a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abd2a-119">PARAMETERS</span></span>

### <span data-ttu-id="abd2a-120">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="abd2a-120">-BusinessIdentities</span></span>
<span data-ttu-id="abd2a-121">Определяет бизнес-удостоверения партнера по интеграции учетной записи.</span><span class="sxs-lookup"><span data-stu-id="abd2a-121">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="abd2a-122">Укажите hash table.</span><span class="sxs-lookup"><span data-stu-id="abd2a-122">Specify a hash table.</span></span>

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

### <span data-ttu-id="abd2a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abd2a-123">-DefaultProfile</span></span>
<span data-ttu-id="abd2a-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="abd2a-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abd2a-125">-Force</span><span class="sxs-lookup"><span data-stu-id="abd2a-125">-Force</span></span>
<span data-ttu-id="abd2a-126">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="abd2a-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="abd2a-127">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="abd2a-127">-Metadata</span></span>
<span data-ttu-id="abd2a-128">Определяет объект метаданных партнера.</span><span class="sxs-lookup"><span data-stu-id="abd2a-128">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="abd2a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="abd2a-129">-Name</span></span>
<span data-ttu-id="abd2a-130">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="abd2a-130">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="abd2a-131">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="abd2a-131">-PartnerName</span></span>
<span data-ttu-id="abd2a-132">Указывает имя партнера по учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="abd2a-132">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="abd2a-133">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="abd2a-133">-PartnerType</span></span>
<span data-ttu-id="abd2a-134">Тип учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="abd2a-134">Specifies the type of the integration account.</span></span>
<span data-ttu-id="abd2a-135">Этот параметр поддерживает тип B2B.</span><span class="sxs-lookup"><span data-stu-id="abd2a-135">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="abd2a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abd2a-136">-ResourceGroupName</span></span>
<span data-ttu-id="abd2a-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="abd2a-137">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="abd2a-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="abd2a-138">-Confirm</span></span>
<span data-ttu-id="abd2a-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abd2a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abd2a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abd2a-140">-WhatIf</span></span>
<span data-ttu-id="abd2a-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abd2a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abd2a-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="abd2a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abd2a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd2a-143">CommonParameters</span></span>
<span data-ttu-id="abd2a-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abd2a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd2a-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abd2a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd2a-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="abd2a-146">INPUTS</span></span>

### <span data-ttu-id="abd2a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="abd2a-147">System.String</span></span>

## <span data-ttu-id="abd2a-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="abd2a-148">OUTPUTS</span></span>

### <span data-ttu-id="abd2a-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="abd2a-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="abd2a-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="abd2a-150">NOTES</span></span>

## <span data-ttu-id="abd2a-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="abd2a-151">RELATED LINKS</span></span>

[<span data-ttu-id="abd2a-152">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="abd2a-152">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="abd2a-153">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="abd2a-153">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="abd2a-154">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="abd2a-154">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)


