---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: daf4631041093b10a1bf712649de8b5c3ad3b6d9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404026"
---
# <span data-ttu-id="a1830-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="a1830-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="a1830-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1830-102">SYNOPSIS</span></span>
<span data-ttu-id="a1830-103">Получить политику WAF</span><span class="sxs-lookup"><span data-stu-id="a1830-103">Get WAF policy</span></span>

## <span data-ttu-id="a1830-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a1830-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1830-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1830-105">DESCRIPTION</span></span>
<span data-ttu-id="a1830-106">Для **get-AzFrontDoorWafPolicy** cmdletGet получает политику WAF в группе ресурсов в рамках текущей подписки</span><span class="sxs-lookup"><span data-stu-id="a1830-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="a1830-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a1830-107">EXAMPLES</span></span>

### <span data-ttu-id="a1830-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a1830-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="a1830-109">Получите политику WAF, которая называется $policyName в $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1830-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="a1830-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a1830-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="a1830-111">Получить всю политику WAF в $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1830-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="a1830-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1830-112">PARAMETERS</span></span>

### <span data-ttu-id="a1830-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1830-113">-DefaultProfile</span></span>
<span data-ttu-id="a1830-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1830-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1830-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a1830-115">-Name</span></span>
<span data-ttu-id="a1830-116">Имя FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="a1830-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="a1830-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1830-117">-ResourceGroupName</span></span>
<span data-ttu-id="a1830-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1830-118">The resource group name.</span></span>

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

### <span data-ttu-id="a1830-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1830-119">CommonParameters</span></span>
<span data-ttu-id="a1830-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1830-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1830-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1830-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1830-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1830-122">INPUTS</span></span>

### <span data-ttu-id="a1830-123">Нет</span><span class="sxs-lookup"><span data-stu-id="a1830-123">None</span></span>

## <span data-ttu-id="a1830-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a1830-124">OUTPUTS</span></span>

### <span data-ttu-id="a1830-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="a1830-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="a1830-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a1830-126">NOTES</span></span>

## <span data-ttu-id="a1830-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1830-127">RELATED LINKS</span></span>

<span data-ttu-id="a1830-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="a1830-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
