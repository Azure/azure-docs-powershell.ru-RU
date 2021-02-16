---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: e824c32ae2ae4f28972cdac9446eeeae6e410c75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242381"
---
# <span data-ttu-id="bed40-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="bed40-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="bed40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bed40-102">SYNOPSIS</span></span>
<span data-ttu-id="bed40-103">Создание пользовательских ресурсов для решения безопасности iOT</span><span class="sxs-lookup"><span data-stu-id="bed40-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="bed40-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bed40-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bed40-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bed40-105">DESCRIPTION</span></span>
<span data-ttu-id="bed40-106">Для решения безопасности iOT создается новый объект ресурсов AzIotSecuritySolutionUserDefinedResourcesObject.</span><span class="sxs-lookup"><span data-stu-id="bed40-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="bed40-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bed40-107">EXAMPLES</span></span>

### <span data-ttu-id="bed40-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bed40-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="bed40-109">Создание ресурсов, определенных пользователем</span><span class="sxs-lookup"><span data-stu-id="bed40-109">Create new user defined resources</span></span>

## <span data-ttu-id="bed40-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bed40-110">PARAMETERS</span></span>

### <span data-ttu-id="bed40-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bed40-111">-DefaultProfile</span></span>
<span data-ttu-id="bed40-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bed40-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bed40-113">-Query</span><span class="sxs-lookup"><span data-stu-id="bed40-113">-Query</span></span>
<span data-ttu-id="bed40-114">Запрос.</span><span class="sxs-lookup"><span data-stu-id="bed40-114">Query.</span></span>

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

### <span data-ttu-id="bed40-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="bed40-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="bed40-116">Запрос подписок.</span><span class="sxs-lookup"><span data-stu-id="bed40-116">Query subscriptions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed40-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bed40-117">CommonParameters</span></span>
<span data-ttu-id="bed40-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bed40-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bed40-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bed40-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bed40-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bed40-120">INPUTS</span></span>

### <span data-ttu-id="bed40-121">Нет</span><span class="sxs-lookup"><span data-stu-id="bed40-121">None</span></span>

## <span data-ttu-id="bed40-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bed40-122">OUTPUTS</span></span>

### <span data-ttu-id="bed40-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="bed40-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="bed40-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bed40-124">NOTES</span></span>

## <span data-ttu-id="bed40-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bed40-125">RELATED LINKS</span></span>
