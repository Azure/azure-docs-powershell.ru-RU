---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 83f2c49eb696ac4e3fef0f411b79af24ae95f56c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954691"
---
# <span data-ttu-id="b467a-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="b467a-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="b467a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b467a-102">SYNOPSIS</span></span>
<span data-ttu-id="b467a-103">Получить политику WAF</span><span class="sxs-lookup"><span data-stu-id="b467a-103">Get WAF policy</span></span>

## <span data-ttu-id="b467a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b467a-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b467a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b467a-105">DESCRIPTION</span></span>
<span data-ttu-id="b467a-106">Для **get-AzFrontDoorWafPolicy** cmdletGet получает политику WAF в группе ресурсов в рамках текущей подписки</span><span class="sxs-lookup"><span data-stu-id="b467a-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="b467a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b467a-107">EXAMPLES</span></span>

### <span data-ttu-id="b467a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b467a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="b467a-109">Получите политику WAF, которая $policyName в $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b467a-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="b467a-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b467a-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="b467a-111">Получить всю политику WAF в $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b467a-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="b467a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b467a-112">PARAMETERS</span></span>

### <span data-ttu-id="b467a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b467a-113">-DefaultProfile</span></span>
<span data-ttu-id="b467a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b467a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b467a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b467a-115">-Name</span></span>
<span data-ttu-id="b467a-116">Имя FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="b467a-116">FireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b467a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b467a-117">-ResourceGroupName</span></span>
<span data-ttu-id="b467a-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b467a-118">The resource group name.</span></span>

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

### <span data-ttu-id="b467a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b467a-119">CommonParameters</span></span>
<span data-ttu-id="b467a-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b467a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b467a-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b467a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b467a-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b467a-122">INPUTS</span></span>

### <span data-ttu-id="b467a-123">Нет</span><span class="sxs-lookup"><span data-stu-id="b467a-123">None</span></span>

## <span data-ttu-id="b467a-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b467a-124">OUTPUTS</span></span>

### <span data-ttu-id="b467a-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="b467a-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="b467a-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b467a-126">NOTES</span></span>

## <span data-ttu-id="b467a-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b467a-127">RELATED LINKS</span></span>

<span data-ttu-id="b467a-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="b467a-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>
