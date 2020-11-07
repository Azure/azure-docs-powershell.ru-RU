---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: fc7acc34a018361b3ebaff67e57221c250e19771
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733714"
---
# <span data-ttu-id="a1e09-101">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a1e09-101">Remove-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="a1e09-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1e09-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e09-103">Удаляет схему учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a1e09-103">Removes an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1e09-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1e09-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1e09-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1e09-105">DESCRIPTION</span></span>
<span data-ttu-id="a1e09-106">Командлет **Remove-AzureRmIntegrationAccountSchema** удаляет схему учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1e09-106">The **Remove-AzureRmIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="a1e09-107">Указание имени учетной записи интеграции, имени группы ресурсов и имени схемы.</span><span class="sxs-lookup"><span data-stu-id="a1e09-107">Specifying the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="a1e09-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="a1e09-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a1e09-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="a1e09-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a1e09-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="a1e09-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a1e09-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="a1e09-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a1e09-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1e09-112">EXAMPLES</span></span>

### <span data-ttu-id="a1e09-113">Пример 1: удаление схемы учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="a1e09-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="a1e09-114">Эта команда удаляет схему учетной записи интеграции с именем IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="a1e09-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="a1e09-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1e09-115">PARAMETERS</span></span>

### <span data-ttu-id="a1e09-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a1e09-116">-Force</span></span>
<span data-ttu-id="a1e09-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a1e09-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a1e09-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1e09-118">-Name</span></span>
<span data-ttu-id="a1e09-119">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a1e09-119">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1e09-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e09-120">-ResourceGroupName</span></span>
<span data-ttu-id="a1e09-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1e09-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a1e09-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a1e09-122">-SchemaName</span></span>
<span data-ttu-id="a1e09-123">Указывает имя схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a1e09-123">Specifies the name of an integration account schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1e09-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1e09-124">-Confirm</span></span>
<span data-ttu-id="a1e09-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a1e09-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1e09-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1e09-126">-WhatIf</span></span>
<span data-ttu-id="a1e09-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a1e09-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1e09-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a1e09-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1e09-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e09-129">-DefaultProfile</span></span>
<span data-ttu-id="a1e09-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1e09-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1e09-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e09-131">CommonParameters</span></span>
<span data-ttu-id="a1e09-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1e09-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e09-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1e09-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e09-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1e09-134">INPUTS</span></span>

## <span data-ttu-id="a1e09-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1e09-135">OUTPUTS</span></span>

## <span data-ttu-id="a1e09-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1e09-136">NOTES</span></span>

## <span data-ttu-id="a1e09-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1e09-137">RELATED LINKS</span></span>

[<span data-ttu-id="a1e09-138">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a1e09-138">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="a1e09-139">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a1e09-139">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="a1e09-140">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a1e09-140">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


