---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 7328eda5e6821b7c403bf949460747fbf7d215e7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913244"
---
# <span data-ttu-id="33e98-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="33e98-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="33e98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="33e98-102">SYNOPSIS</span></span>
<span data-ttu-id="33e98-103">Получает общие ключи для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="33e98-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="33e98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="33e98-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33e98-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33e98-105">DESCRIPTION</span></span>
<span data-ttu-id="33e98-106">Командлет **Get-AzOperationalInsightsWorkspaceSharedKey** перечисляет общие ключи для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="33e98-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="33e98-107">Ключи используются для соединения агентов оперативной аналитики с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="33e98-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="33e98-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="33e98-108">EXAMPLES</span></span>

### <span data-ttu-id="33e98-109">Пример 1: получение общих ключей с помощью имени рабочей области</span><span class="sxs-lookup"><span data-stu-id="33e98-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="33e98-110">Эта команда получает общие ключи для рабочей области с именем MyWorkspace в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="33e98-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="33e98-111">Пример 2: получение общих ключей с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="33e98-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="33e98-112">Эта команда получает рабочую область с именем MyWorkspace с помощью командлета Get-AzOperationalInsightsWorkspace, а затем передает рабочую область командлету **Get-AzOperationalInsightsWorkspaceSharedKey** .</span><span class="sxs-lookup"><span data-stu-id="33e98-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="33e98-113">Команда получает общие ключи для этой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="33e98-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="33e98-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="33e98-114">PARAMETERS</span></span>

### <span data-ttu-id="33e98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33e98-115">-DefaultProfile</span></span>
<span data-ttu-id="33e98-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="33e98-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33e98-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="33e98-117">-Name</span></span>
<span data-ttu-id="33e98-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="33e98-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="33e98-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33e98-119">-ResourceGroupName</span></span>
<span data-ttu-id="33e98-120">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="33e98-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="33e98-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33e98-121">CommonParameters</span></span>
<span data-ttu-id="33e98-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="33e98-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33e98-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33e98-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33e98-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="33e98-124">INPUTS</span></span>

### <span data-ttu-id="33e98-125">System. String</span><span class="sxs-lookup"><span data-stu-id="33e98-125">System.String</span></span>

## <span data-ttu-id="33e98-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33e98-126">OUTPUTS</span></span>

### <span data-ttu-id="33e98-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="33e98-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="33e98-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="33e98-128">NOTES</span></span>

## <span data-ttu-id="33e98-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33e98-129">RELATED LINKS</span></span>

[<span data-ttu-id="33e98-130">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="33e98-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="33e98-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="33e98-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


