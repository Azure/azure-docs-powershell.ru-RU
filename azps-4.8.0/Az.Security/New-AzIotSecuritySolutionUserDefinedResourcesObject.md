---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: e824c32ae2ae4f28972cdac9446eeeae6e410c75
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243981"
---
# <span data-ttu-id="0ba9b-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="0ba9b-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="0ba9b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ba9b-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba9b-103">Создание новых ресурсов, определенных пользователем, для решения безопасности IOT</span><span class="sxs-lookup"><span data-stu-id="0ba9b-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="0ba9b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ba9b-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ba9b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ba9b-105">DESCRIPTION</span></span>
<span data-ttu-id="0ba9b-106">Командлет AzIotSecuritySolutionUserDefinedResourcesObject создает новый объект ресурсов, определяемый пользователем, для решения безопасности IOT.</span><span class="sxs-lookup"><span data-stu-id="0ba9b-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="0ba9b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ba9b-107">EXAMPLES</span></span>

### <span data-ttu-id="0ba9b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0ba9b-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="0ba9b-109">Создание новых ресурсов, определенных пользователем</span><span class="sxs-lookup"><span data-stu-id="0ba9b-109">Create new user defined resources</span></span>

## <span data-ttu-id="0ba9b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ba9b-110">PARAMETERS</span></span>

### <span data-ttu-id="0ba9b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ba9b-111">-DefaultProfile</span></span>
<span data-ttu-id="0ba9b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ba9b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ba9b-113">-Query</span><span class="sxs-lookup"><span data-stu-id="0ba9b-113">-Query</span></span>
<span data-ttu-id="0ba9b-114">Запроса.</span><span class="sxs-lookup"><span data-stu-id="0ba9b-114">Query.</span></span>

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

### <span data-ttu-id="0ba9b-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="0ba9b-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="0ba9b-116">Подписка на запросы.</span><span class="sxs-lookup"><span data-stu-id="0ba9b-116">Query subscriptions.</span></span>

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

### <span data-ttu-id="0ba9b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba9b-117">CommonParameters</span></span>
<span data-ttu-id="0ba9b-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ba9b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba9b-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ba9b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba9b-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ba9b-120">INPUTS</span></span>

### <span data-ttu-id="0ba9b-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="0ba9b-121">None</span></span>

## <span data-ttu-id="0ba9b-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ba9b-122">OUTPUTS</span></span>

### <span data-ttu-id="0ba9b-123">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="0ba9b-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="0ba9b-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ba9b-124">NOTES</span></span>

## <span data-ttu-id="0ba9b-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ba9b-125">RELATED LINKS</span></span>
