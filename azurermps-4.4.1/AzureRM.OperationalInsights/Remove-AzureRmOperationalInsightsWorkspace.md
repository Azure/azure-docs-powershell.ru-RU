---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 3f7ed1a36cc95296ee7fdeec45c5039063032d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559587"
---
# <span data-ttu-id="1271a-101">Remove-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1271a-101">Remove-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="1271a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1271a-102">SYNOPSIS</span></span>
<span data-ttu-id="1271a-103">Удаление рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1271a-103">Removes a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1271a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1271a-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1271a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1271a-105">DESCRIPTION</span></span>
<span data-ttu-id="1271a-106">Командлет **Remove-AzureRmOperationalInsightsWorkspace** удаляет существующую рабочую область.</span><span class="sxs-lookup"><span data-stu-id="1271a-106">The **Remove-AzureRmOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="1271a-107">Если эта Рабочая область была связана с существующей учетной записью с помощью параметра *CustomerID* на этапе создания, исходная учетная запись не будет удалена на портале оперативной аналитики.</span><span class="sxs-lookup"><span data-stu-id="1271a-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="1271a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1271a-108">EXAMPLES</span></span>

### <span data-ttu-id="1271a-109">Пример 1: Удаление рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="1271a-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="1271a-110">Эта команда удаляет рабочую область с именем MyWorkspace из группы ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1271a-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="1271a-111">Пример 2: Удаление рабочей области с помощью конвейера и без подтверждения</span><span class="sxs-lookup"><span data-stu-id="1271a-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzureRmOperationalInsightsWorkspace -Force
```

<span data-ttu-id="1271a-112">Эта команда использует командлет Get-AzureRmOperationalInsightsWorkspace, чтобы получить рабочую область с именем MyWorkspace, а затем передает ее командлету **Remove-AzureRmOperationalInsightsWorkspace** с помощью оператора конвейера, чтобы удалить его.</span><span class="sxs-lookup"><span data-stu-id="1271a-112">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="1271a-113">Так как параметр *Force* задан, команда не выдает запрос перед удалением рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1271a-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="1271a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1271a-114">PARAMETERS</span></span>

### <span data-ttu-id="1271a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1271a-115">-Force</span></span>
<span data-ttu-id="1271a-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1271a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1271a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1271a-117">-Name</span></span>
<span data-ttu-id="1271a-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1271a-118">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1271a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1271a-119">-ResourceGroupName</span></span>
<span data-ttu-id="1271a-120">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="1271a-120">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1271a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1271a-121">-Confirm</span></span>
<span data-ttu-id="1271a-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1271a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1271a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1271a-123">-WhatIf</span></span>
<span data-ttu-id="1271a-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1271a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1271a-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1271a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1271a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1271a-126">-DefaultProfile</span></span>
<span data-ttu-id="1271a-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1271a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1271a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1271a-128">CommonParameters</span></span>
<span data-ttu-id="1271a-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1271a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1271a-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1271a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1271a-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1271a-131">INPUTS</span></span>

## <span data-ttu-id="1271a-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1271a-132">OUTPUTS</span></span>

## <span data-ttu-id="1271a-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="1271a-133">NOTES</span></span>

## <span data-ttu-id="1271a-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1271a-134">RELATED LINKS</span></span>

[<span data-ttu-id="1271a-135">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="1271a-135">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="1271a-136">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1271a-136">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


