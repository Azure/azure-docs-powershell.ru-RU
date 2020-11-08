---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235151"
---
# <span data-ttu-id="128d8-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="128d8-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="128d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="128d8-102">SYNOPSIS</span></span>
<span data-ttu-id="128d8-103">Остановите туннель SSH Kubectl, созданный в Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="128d8-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="128d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="128d8-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="128d8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="128d8-105">DESCRIPTION</span></span>
<span data-ttu-id="128d8-106">Остановите туннель SSH Kubectl, созданный в Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="128d8-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="128d8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="128d8-107">EXAMPLES</span></span>

### <span data-ttu-id="128d8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="128d8-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="128d8-109">Останавливает существующую настройку туннеля SSH, выполняя Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="128d8-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="128d8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="128d8-110">PARAMETERS</span></span>

### <span data-ttu-id="128d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="128d8-111">-DefaultProfile</span></span>
<span data-ttu-id="128d8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="128d8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="128d8-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="128d8-113">-PassThru</span></span>
<span data-ttu-id="128d8-114">Возвращает значение истина, если закрытие туннеля SSH закрыто.</span><span class="sxs-lookup"><span data-stu-id="128d8-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="128d8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="128d8-115">CommonParameters</span></span>
<span data-ttu-id="128d8-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="128d8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="128d8-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="128d8-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="128d8-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="128d8-118">INPUTS</span></span>

### <span data-ttu-id="128d8-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="128d8-119">None</span></span>

## <span data-ttu-id="128d8-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="128d8-120">OUTPUTS</span></span>

### <span data-ttu-id="128d8-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="128d8-121">System.Boolean</span></span>

## <span data-ttu-id="128d8-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="128d8-122">NOTES</span></span>

## <span data-ttu-id="128d8-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="128d8-123">RELATED LINKS</span></span>
