---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
ms.openlocfilehash: a3a3fc16b253235da82626ab6d827d074f05860d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078206"
---
# <span data-ttu-id="550c8-101">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="550c8-101">New-AzIntegrationAccount</span></span>

## <span data-ttu-id="550c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="550c8-102">SYNOPSIS</span></span>
<span data-ttu-id="550c8-103">Создание учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="550c8-103">Creates an integration account.</span></span>

## <span data-ttu-id="550c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="550c8-104">SYNTAX</span></span>

```
New-AzIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="550c8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="550c8-105">DESCRIPTION</span></span>
<span data-ttu-id="550c8-106">Командлет **New-AzIntegrationAccount** создает учетную запись интеграции.</span><span class="sxs-lookup"><span data-stu-id="550c8-106">The **New-AzIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="550c8-107">Этот командлет возвращает объект, представляющий учетную запись интеграции. Укажите имя, расположение, имя группы ресурсов и название SKU.</span><span class="sxs-lookup"><span data-stu-id="550c8-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="550c8-108">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="550c8-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="550c8-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="550c8-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="550c8-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="550c8-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="550c8-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="550c8-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="550c8-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="550c8-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="550c8-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="550c8-113">EXAMPLES</span></span>

### <span data-ttu-id="550c8-114">Пример 1: создание учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="550c8-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="550c8-115">Эта команда создает учетную запись интеграции с именем IntegrationAccount31 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="550c8-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="550c8-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="550c8-116">PARAMETERS</span></span>

### <span data-ttu-id="550c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="550c8-117">-DefaultProfile</span></span>
<span data-ttu-id="550c8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="550c8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="550c8-119">-Location</span><span class="sxs-lookup"><span data-stu-id="550c8-119">-Location</span></span>
<span data-ttu-id="550c8-120">Указывает расположение для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="550c8-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="550c8-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="550c8-121">-Name</span></span>
<span data-ttu-id="550c8-122">Указывает имя для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="550c8-122">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="550c8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="550c8-123">-ResourceGroupName</span></span>
<span data-ttu-id="550c8-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="550c8-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="550c8-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="550c8-125">-Sku</span></span>
<span data-ttu-id="550c8-126">Указывает имя SKU для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="550c8-126">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="550c8-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="550c8-127">-Confirm</span></span>
<span data-ttu-id="550c8-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="550c8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="550c8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="550c8-129">-WhatIf</span></span>
<span data-ttu-id="550c8-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="550c8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="550c8-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="550c8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="550c8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="550c8-132">CommonParameters</span></span>
<span data-ttu-id="550c8-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="550c8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="550c8-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="550c8-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="550c8-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="550c8-135">INPUTS</span></span>

### <span data-ttu-id="550c8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="550c8-136">System.String</span></span>

## <span data-ttu-id="550c8-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="550c8-137">OUTPUTS</span></span>

### <span data-ttu-id="550c8-138">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="550c8-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="550c8-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="550c8-139">NOTES</span></span>

## <span data-ttu-id="550c8-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="550c8-140">RELATED LINKS</span></span>

[<span data-ttu-id="550c8-141">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="550c8-141">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="550c8-142">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="550c8-142">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="550c8-143">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="550c8-143">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


