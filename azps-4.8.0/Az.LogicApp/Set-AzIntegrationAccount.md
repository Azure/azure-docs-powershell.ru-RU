---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
ms.openlocfilehash: 3bb20e0314e95f2586c0bd8585c7937c4d6ca5b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236150"
---
# <span data-ttu-id="6db96-101">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="6db96-101">Set-AzIntegrationAccount</span></span>

## <span data-ttu-id="6db96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6db96-102">SYNOPSIS</span></span>
<span data-ttu-id="6db96-103">Изменение учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6db96-103">Modifies an integration account.</span></span>

## <span data-ttu-id="6db96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6db96-104">SYNTAX</span></span>

```
Set-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6db96-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6db96-105">DESCRIPTION</span></span>
<span data-ttu-id="6db96-106">Командлет **Set-AzIntegrationAccount** изменяет учетную запись интеграции.</span><span class="sxs-lookup"><span data-stu-id="6db96-106">The **Set-AzIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="6db96-107">Этот командлет возвращает объект, представляющий учетную запись интеграции.</span><span class="sxs-lookup"><span data-stu-id="6db96-107">This cmdlet returns an object that represents the integration account.</span></span>
<span data-ttu-id="6db96-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="6db96-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6db96-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="6db96-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6db96-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="6db96-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6db96-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="6db96-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6db96-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6db96-112">EXAMPLES</span></span>

### <span data-ttu-id="6db96-113">Пример 1: изменение учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="6db96-113">Example 1: Modify an integration account</span></span>
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

<span data-ttu-id="6db96-114">Эта команда изменяет учетную запись интеграции с именем IntegrationAccount31 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6db96-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="6db96-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6db96-115">PARAMETERS</span></span>

### <span data-ttu-id="6db96-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db96-116">-DefaultProfile</span></span>
<span data-ttu-id="6db96-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6db96-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6db96-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6db96-118">-Force</span></span>
<span data-ttu-id="6db96-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="6db96-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6db96-120">-Location</span><span class="sxs-lookup"><span data-stu-id="6db96-120">-Location</span></span>
<span data-ttu-id="6db96-121">Указывает расположение для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6db96-121">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="6db96-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6db96-122">-Name</span></span>
<span data-ttu-id="6db96-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6db96-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="6db96-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6db96-124">-ResourceGroupName</span></span>
<span data-ttu-id="6db96-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6db96-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6db96-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="6db96-126">-Sku</span></span>
<span data-ttu-id="6db96-127">Указывает имя SKU для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6db96-127">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="6db96-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6db96-128">-Confirm</span></span>
<span data-ttu-id="6db96-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6db96-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6db96-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6db96-130">-WhatIf</span></span>
<span data-ttu-id="6db96-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6db96-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6db96-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6db96-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6db96-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db96-133">CommonParameters</span></span>
<span data-ttu-id="6db96-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6db96-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db96-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6db96-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db96-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6db96-136">INPUTS</span></span>

### <span data-ttu-id="6db96-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6db96-137">System.String</span></span>

## <span data-ttu-id="6db96-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6db96-138">OUTPUTS</span></span>

### <span data-ttu-id="6db96-139">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="6db96-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="6db96-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="6db96-140">NOTES</span></span>

## <span data-ttu-id="6db96-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6db96-141">RELATED LINKS</span></span>

[<span data-ttu-id="6db96-142">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="6db96-142">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="6db96-143">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="6db96-143">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="6db96-144">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="6db96-144">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

