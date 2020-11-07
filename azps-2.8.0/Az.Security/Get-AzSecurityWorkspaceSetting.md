---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 274a751130d5dba8d246a2f02f72be815f889378
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903898"
---
# <span data-ttu-id="9ffb0-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="9ffb0-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="9ffb0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ffb0-102">SYNOPSIS</span></span>
<span data-ttu-id="9ffb0-103">Получает настроенные параметры рабочей области безопасности в подписке.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="9ffb0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ffb0-104">SYNTAX</span></span>

### <span data-ttu-id="9ffb0-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ffb0-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ffb0-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="9ffb0-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ffb0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ffb0-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ffb0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ffb0-108">DESCRIPTION</span></span>
<span data-ttu-id="9ffb0-109">Этот командлет позволяет найти настроенную рабочую область, в которой будут храниться данные безопасности, собранные агентом безопасности, который установлен в виртуальных машинах в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="9ffb0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ffb0-110">EXAMPLES</span></span>

### <span data-ttu-id="9ffb0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9ffb0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="9ffb0-112">Получает параметры рабочей области для подписки.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="9ffb0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ffb0-113">PARAMETERS</span></span>

### <span data-ttu-id="9ffb0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ffb0-114">-DefaultProfile</span></span>
<span data-ttu-id="9ffb0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ffb0-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9ffb0-116">-Name</span></span>
<span data-ttu-id="9ffb0-117">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-117">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ffb0-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ffb0-118">-ResourceId</span></span>
<span data-ttu-id="9ffb0-119">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-119">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ffb0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ffb0-120">CommonParameters</span></span>
<span data-ttu-id="9ffb0-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ffb0-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ffb0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ffb0-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ffb0-123">INPUTS</span></span>

### <span data-ttu-id="9ffb0-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9ffb0-124">System.String</span></span>

## <span data-ttu-id="9ffb0-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ffb0-125">OUTPUTS</span></span>

### <span data-ttu-id="9ffb0-126">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="9ffb0-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="9ffb0-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ffb0-127">NOTES</span></span>

## <span data-ttu-id="9ffb0-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ffb0-128">RELATED LINKS</span></span>
