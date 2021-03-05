---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 633173a0ce8814ee2af9300be5b1cfc19bdf9a5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975635"
---
# <span data-ttu-id="43301-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="43301-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="43301-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43301-102">SYNOPSIS</span></span>
<span data-ttu-id="43301-103">Остановить SSH-туннель Kubectl, созданный в start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="43301-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="43301-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="43301-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43301-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43301-105">DESCRIPTION</span></span>
<span data-ttu-id="43301-106">Остановить SSH-туннель Kubectl, созданный в start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="43301-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="43301-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="43301-107">EXAMPLES</span></span>

### <span data-ttu-id="43301-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43301-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="43301-109">Останавливает существующую настройку SSH-туннель, выполняя Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="43301-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="43301-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43301-110">PARAMETERS</span></span>

### <span data-ttu-id="43301-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43301-111">-DefaultProfile</span></span>
<span data-ttu-id="43301-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43301-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43301-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43301-113">-PassThru</span></span>
<span data-ttu-id="43301-114">Возвращает true, если SSH-туннель закрыт.</span><span class="sxs-lookup"><span data-stu-id="43301-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="43301-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43301-115">CommonParameters</span></span>
<span data-ttu-id="43301-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43301-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43301-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43301-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43301-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43301-118">INPUTS</span></span>

### <span data-ttu-id="43301-119">Нет</span><span class="sxs-lookup"><span data-stu-id="43301-119">None</span></span>

## <span data-ttu-id="43301-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="43301-120">OUTPUTS</span></span>

### <span data-ttu-id="43301-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="43301-121">System.Boolean</span></span>

## <span data-ttu-id="43301-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="43301-122">NOTES</span></span>

## <span data-ttu-id="43301-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43301-123">RELATED LINKS</span></span>
