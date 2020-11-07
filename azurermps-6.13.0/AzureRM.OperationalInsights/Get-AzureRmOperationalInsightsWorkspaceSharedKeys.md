---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacesharedkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
ms.openlocfilehash: 07d0834b89010ff533e1620f29904ea159d3dfea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734129"
---
# <span data-ttu-id="3564b-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span><span class="sxs-lookup"><span data-stu-id="3564b-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span></span>

## <span data-ttu-id="3564b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3564b-102">SYNOPSIS</span></span>
<span data-ttu-id="3564b-103">Получает общие ключи для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3564b-103">Gets the shared keys for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3564b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3564b-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceSharedKeys [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3564b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3564b-105">DESCRIPTION</span></span>
<span data-ttu-id="3564b-106">Командлет **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** перечисляет общие ключи для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3564b-106">The **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="3564b-107">Ключи используются для соединения агентов оперативной аналитики с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="3564b-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="3564b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3564b-108">EXAMPLES</span></span>

### <span data-ttu-id="3564b-109">Пример 1: получение общих ключей с помощью имени рабочей области</span><span class="sxs-lookup"><span data-stu-id="3564b-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceSharedKeys -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="3564b-110">Эта команда получает общие ключи для рабочей области с именем MyWorkspace в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3564b-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="3564b-111">Пример 2: получение общих ключей с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="3564b-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureRmOperationalInsightsWorkspaceSharedKeys
```

<span data-ttu-id="3564b-112">Эта команда получает рабочую область с именем MyWorkspace с помощью командлета Get-AzureRmOperationalInsightsWorkspace, а затем передает рабочую область командлету **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** .</span><span class="sxs-lookup"><span data-stu-id="3564b-112">This command gets the workspace named MyWorkspace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet.</span></span>
<span data-ttu-id="3564b-113">Команда получает общие ключи для этой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3564b-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="3564b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3564b-114">PARAMETERS</span></span>

### <span data-ttu-id="3564b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3564b-115">-DefaultProfile</span></span>
<span data-ttu-id="3564b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3564b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3564b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3564b-117">-Name</span></span>
<span data-ttu-id="3564b-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3564b-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="3564b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3564b-119">-ResourceGroupName</span></span>
<span data-ttu-id="3564b-120">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3564b-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="3564b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3564b-121">CommonParameters</span></span>
<span data-ttu-id="3564b-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3564b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3564b-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3564b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3564b-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3564b-124">INPUTS</span></span>

### <span data-ttu-id="3564b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3564b-125">System.String</span></span>

## <span data-ttu-id="3564b-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3564b-126">OUTPUTS</span></span>

### <span data-ttu-id="3564b-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="3564b-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="3564b-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="3564b-128">NOTES</span></span>

## <span data-ttu-id="3564b-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3564b-129">RELATED LINKS</span></span>

[<span data-ttu-id="3564b-130">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="3564b-130">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="3564b-131">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="3564b-131">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


