---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506978"
---
# <span data-ttu-id="6c76b-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="6c76b-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="6c76b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c76b-102">SYNOPSIS</span></span>
<span data-ttu-id="6c76b-103">Остановить SSH-туннель Kubectl, созданный в start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="6c76b-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="6c76b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6c76b-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c76b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c76b-105">DESCRIPTION</span></span>
<span data-ttu-id="6c76b-106">Остановить SSH-туннель Kubectl, созданный в start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="6c76b-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="6c76b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6c76b-107">EXAMPLES</span></span>

### <span data-ttu-id="6c76b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6c76b-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="6c76b-109">Останавливает существующую настройку SSH-туннель, выполняя Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="6c76b-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="6c76b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c76b-110">PARAMETERS</span></span>

### <span data-ttu-id="6c76b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c76b-111">-DefaultProfile</span></span>
<span data-ttu-id="6c76b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c76b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c76b-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c76b-113">-PassThru</span></span>
<span data-ttu-id="6c76b-114">Возвращается истина, если SSH-туннель закрыт.</span><span class="sxs-lookup"><span data-stu-id="6c76b-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="6c76b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c76b-115">CommonParameters</span></span>
<span data-ttu-id="6c76b-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c76b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c76b-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c76b-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c76b-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c76b-118">INPUTS</span></span>

### <span data-ttu-id="6c76b-119">Нет</span><span class="sxs-lookup"><span data-stu-id="6c76b-119">None</span></span>

## <span data-ttu-id="6c76b-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6c76b-120">OUTPUTS</span></span>

### <span data-ttu-id="6c76b-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6c76b-121">System.Boolean</span></span>

## <span data-ttu-id="6c76b-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6c76b-122">NOTES</span></span>

## <span data-ttu-id="6c76b-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c76b-123">RELATED LINKS</span></span>
