---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
ms.openlocfilehash: 8a6808c19dda99f6d76280fc8519a6afc658d9ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975763"
---
# <span data-ttu-id="e361a-101">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e361a-101">Set-AzIntegrationAccount</span></span>

## <span data-ttu-id="e361a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e361a-102">SYNOPSIS</span></span>
<span data-ttu-id="e361a-103">Изменяет учетную запись интеграции.</span><span class="sxs-lookup"><span data-stu-id="e361a-103">Modifies an integration account.</span></span>

## <span data-ttu-id="e361a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e361a-104">SYNTAX</span></span>

```
Set-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e361a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e361a-105">DESCRIPTION</span></span>
<span data-ttu-id="e361a-106">**Cmdlet Set-AzIntegrationAccount** изменяет учетную запись интеграции.</span><span class="sxs-lookup"><span data-stu-id="e361a-106">The **Set-AzIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="e361a-107">Этот cmdlet возвращает объект, который представляет учетную запись интеграции.</span><span class="sxs-lookup"><span data-stu-id="e361a-107">This cmdlet returns an object that represents the integration account.</span></span>
<span data-ttu-id="e361a-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="e361a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e361a-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="e361a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e361a-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="e361a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e361a-111">Если не задан параметр обязательного шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="e361a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e361a-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e361a-112">EXAMPLES</span></span>

### <span data-ttu-id="e361a-113">Пример 1. Изменение учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="e361a-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="e361a-114">Эта команда изменяет учетную запись интеграции IntegrationAccount31 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e361a-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="e361a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e361a-115">PARAMETERS</span></span>

### <span data-ttu-id="e361a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e361a-116">-DefaultProfile</span></span>
<span data-ttu-id="e361a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e361a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e361a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e361a-118">-Force</span></span>
<span data-ttu-id="e361a-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e361a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e361a-120">-Location</span><span class="sxs-lookup"><span data-stu-id="e361a-120">-Location</span></span>
<span data-ttu-id="e361a-121">Указывает расположение для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e361a-121">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="e361a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e361a-122">-Name</span></span>
<span data-ttu-id="e361a-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e361a-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="e361a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e361a-124">-ResourceGroupName</span></span>
<span data-ttu-id="e361a-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e361a-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e361a-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="e361a-126">-Sku</span></span>
<span data-ttu-id="e361a-127">Указывает имя SKU для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e361a-127">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e361a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e361a-128">-Confirm</span></span>
<span data-ttu-id="e361a-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e361a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e361a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e361a-130">-WhatIf</span></span>
<span data-ttu-id="e361a-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e361a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e361a-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e361a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e361a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e361a-133">CommonParameters</span></span>
<span data-ttu-id="e361a-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e361a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e361a-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e361a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e361a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e361a-136">INPUTS</span></span>

### <span data-ttu-id="e361a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e361a-137">System.String</span></span>

## <span data-ttu-id="e361a-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e361a-138">OUTPUTS</span></span>

### <span data-ttu-id="e361a-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e361a-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="e361a-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e361a-140">NOTES</span></span>

## <span data-ttu-id="e361a-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e361a-141">RELATED LINKS</span></span>

[<span data-ttu-id="e361a-142">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e361a-142">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="e361a-143">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e361a-143">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="e361a-144">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e361a-144">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)


