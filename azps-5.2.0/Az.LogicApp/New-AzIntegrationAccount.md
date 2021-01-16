---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
ms.openlocfilehash: a3a3fc16b253235da82626ab6d827d074f05860d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393756"
---
# <span data-ttu-id="c1c54-101">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c1c54-101">New-AzIntegrationAccount</span></span>

## <span data-ttu-id="c1c54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1c54-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c54-103">Создает учетную запись интеграции.</span><span class="sxs-lookup"><span data-stu-id="c1c54-103">Creates an integration account.</span></span>

## <span data-ttu-id="c1c54-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c1c54-104">SYNTAX</span></span>

```
New-AzIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1c54-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1c54-105">DESCRIPTION</span></span>
<span data-ttu-id="c1c54-106">Для этого создается учетная запись интеграции с **New-AzIntegrationAccount.**</span><span class="sxs-lookup"><span data-stu-id="c1c54-106">The **New-AzIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="c1c54-107">Этот cmdlet возвращает объект, который представляет учетную запись интеграции. Укажите имя, расположение, имя группы ресурсов и имя SKU.</span><span class="sxs-lookup"><span data-stu-id="c1c54-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="c1c54-108">Значения файлов параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="c1c54-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="c1c54-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="c1c54-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c1c54-110">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="c1c54-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c1c54-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="c1c54-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c1c54-112">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="c1c54-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c1c54-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c1c54-113">EXAMPLES</span></span>

### <span data-ttu-id="c1c54-114">Пример 1. Создание учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="c1c54-114">Example 1: Create an integration account</span></span>
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

<span data-ttu-id="c1c54-115">Эта команда создает учетную запись интеграции с именем IntegrationAccount31 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c1c54-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="c1c54-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1c54-116">PARAMETERS</span></span>

### <span data-ttu-id="c1c54-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c54-117">-DefaultProfile</span></span>
<span data-ttu-id="c1c54-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c1c54-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1c54-119">-Location</span><span class="sxs-lookup"><span data-stu-id="c1c54-119">-Location</span></span>
<span data-ttu-id="c1c54-120">Указывает расположение для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c1c54-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="c1c54-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c1c54-121">-Name</span></span>
<span data-ttu-id="c1c54-122">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c1c54-122">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="c1c54-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1c54-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1c54-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c1c54-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c1c54-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="c1c54-125">-Sku</span></span>
<span data-ttu-id="c1c54-126">Указывает имя SKU для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c1c54-126">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="c1c54-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1c54-127">-Confirm</span></span>
<span data-ttu-id="c1c54-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1c54-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1c54-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1c54-129">-WhatIf</span></span>
<span data-ttu-id="c1c54-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1c54-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1c54-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c1c54-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1c54-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c54-132">CommonParameters</span></span>
<span data-ttu-id="c1c54-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1c54-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c54-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1c54-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c54-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1c54-135">INPUTS</span></span>

### <span data-ttu-id="c1c54-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c1c54-136">System.String</span></span>

## <span data-ttu-id="c1c54-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c1c54-137">OUTPUTS</span></span>

### <span data-ttu-id="c1c54-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c1c54-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="c1c54-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c1c54-139">NOTES</span></span>

## <span data-ttu-id="c1c54-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1c54-140">RELATED LINKS</span></span>

[<span data-ttu-id="c1c54-141">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c1c54-141">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="c1c54-142">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c1c54-142">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="c1c54-143">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c1c54-143">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


