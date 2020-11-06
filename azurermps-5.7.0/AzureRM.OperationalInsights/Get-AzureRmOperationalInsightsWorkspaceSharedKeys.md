---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacesharedkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
ms.openlocfilehash: 5fab6a3a0419047fef32f5bf32f52e1f7ee57d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560239"
---
# <span data-ttu-id="f7811-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span><span class="sxs-lookup"><span data-stu-id="f7811-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span></span>

## <span data-ttu-id="f7811-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7811-102">SYNOPSIS</span></span>
<span data-ttu-id="f7811-103">Получает общие ключи для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f7811-103">Gets the shared keys for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7811-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7811-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceSharedKeys [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7811-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7811-105">DESCRIPTION</span></span>
<span data-ttu-id="f7811-106">Командлет **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** перечисляет общие ключи для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f7811-106">The **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="f7811-107">Ключи используются для соединения агентов оперативной аналитики с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="f7811-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="f7811-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7811-108">EXAMPLES</span></span>

### <span data-ttu-id="f7811-109">Пример 1: получение общих ключей с помощью имени рабочей области</span><span class="sxs-lookup"><span data-stu-id="f7811-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceSharedKeys -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="f7811-110">Эта команда получает общие ключи для рабочей области с именем MyWorkspace в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f7811-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="f7811-111">Пример 2: получение общих ключей с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="f7811-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureRmOperationalInsightsWorkspaceSharedKeys
```

<span data-ttu-id="f7811-112">Эта команда получает рабочую область с именем MyWorkspace с помощью командлета Get-AzureRmOperationalInsightsWorkspace, а затем передает рабочую область командлету **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** .</span><span class="sxs-lookup"><span data-stu-id="f7811-112">This command gets the workspace named MyWorkspace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet.</span></span>
<span data-ttu-id="f7811-113">Команда получает общие ключи для этой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f7811-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="f7811-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7811-114">PARAMETERS</span></span>

### <span data-ttu-id="f7811-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7811-115">-DefaultProfile</span></span>
<span data-ttu-id="f7811-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f7811-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7811-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f7811-117">-Name</span></span>
<span data-ttu-id="f7811-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f7811-118">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7811-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7811-119">-ResourceGroupName</span></span>
<span data-ttu-id="f7811-120">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f7811-120">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7811-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7811-121">CommonParameters</span></span>
<span data-ttu-id="f7811-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7811-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7811-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7811-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7811-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7811-124">INPUTS</span></span>

### <span data-ttu-id="f7811-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="f7811-125">None</span></span>
<span data-ttu-id="f7811-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f7811-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7811-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7811-127">OUTPUTS</span></span>

### <span data-ttu-id="f7811-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="f7811-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="f7811-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7811-129">NOTES</span></span>

## <span data-ttu-id="f7811-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7811-130">RELATED LINKS</span></span>

[<span data-ttu-id="f7811-131">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="f7811-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="f7811-132">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f7811-132">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


