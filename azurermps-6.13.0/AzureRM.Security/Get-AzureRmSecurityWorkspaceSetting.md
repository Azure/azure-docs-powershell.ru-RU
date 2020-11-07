---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 7e2a655810c885245d3694fb63caa44c5b4119e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732902"
---
# <span data-ttu-id="f3c3d-101">Get-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="f3c3d-101">Get-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="f3c3d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c3d-103">Получает настроенные параметры рабочей области безопасности в подписке.</span><span class="sxs-lookup"><span data-stu-id="f3c3d-103">Gets the configured security workspace settings on a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3c3d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3c3d-104">SYNTAX</span></span>

### <span data-ttu-id="f3c3d-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f3c3d-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3c3d-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="f3c3d-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3c3d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3c3d-107">ResourceId</span></span>
```
Get-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3c3d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3c3d-108">DESCRIPTION</span></span>
<span data-ttu-id="f3c3d-109">Этот командлет позволяет найти настроенную рабочую область, в которой будут храниться данные безопасности, собранные агентом безопасности, который установлен в виртуальных машинах в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="f3c3d-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="f3c3d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3c3d-110">EXAMPLES</span></span>

### <span data-ttu-id="f3c3d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f3c3d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="f3c3d-112">Получает параметры рабочей области для подписки.</span><span class="sxs-lookup"><span data-stu-id="f3c3d-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="f3c3d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3c3d-113">PARAMETERS</span></span>

### <span data-ttu-id="f3c3d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c3d-114">-DefaultProfile</span></span>
<span data-ttu-id="f3c3d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3c3d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3c3d-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f3c3d-116">-Name</span></span>
<span data-ttu-id="f3c3d-117">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f3c3d-117">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3d-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3c3d-118">-ResourceId</span></span>
<span data-ttu-id="f3c3d-119">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="f3c3d-119">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c3d-120">CommonParameters</span></span>
<span data-ttu-id="f3c3d-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3c3d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c3d-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3c3d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c3d-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3c3d-123">INPUTS</span></span>

### <span data-ttu-id="f3c3d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f3c3d-124">System.String</span></span>

## <span data-ttu-id="f3c3d-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3c3d-125">OUTPUTS</span></span>

### <span data-ttu-id="f3c3d-126">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="f3c3d-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="f3c3d-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3c3d-127">NOTES</span></span>

## <span data-ttu-id="f3c3d-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3c3d-128">RELATED LINKS</span></span>
