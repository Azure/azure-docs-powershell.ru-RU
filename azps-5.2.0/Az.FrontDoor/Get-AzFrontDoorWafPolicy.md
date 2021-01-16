---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ea1ace189271c96bbf4bda0bc67385c678ef3c40
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404612"
---
# <span data-ttu-id="cb325-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="cb325-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="cb325-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb325-102">SYNOPSIS</span></span>
<span data-ttu-id="cb325-103">Получить политику WAF</span><span class="sxs-lookup"><span data-stu-id="cb325-103">Get WAF policy</span></span>

## <span data-ttu-id="cb325-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cb325-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb325-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb325-105">DESCRIPTION</span></span>
<span data-ttu-id="cb325-106">Для **get-AzFrontDoorWafPolicy** cmdletGet получает политику WAF в группе ресурсов в рамках текущей подписки</span><span class="sxs-lookup"><span data-stu-id="cb325-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="cb325-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cb325-107">EXAMPLES</span></span>

### <span data-ttu-id="cb325-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb325-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="cb325-109">Получите политику WAF, которая $policyName в $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb325-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="cb325-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cb325-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="cb325-111">Получить всю политику WAF в $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb325-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="cb325-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb325-112">PARAMETERS</span></span>

### <span data-ttu-id="cb325-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb325-113">-DefaultProfile</span></span>
<span data-ttu-id="cb325-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb325-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb325-115">-Name</span><span class="sxs-lookup"><span data-stu-id="cb325-115">-Name</span></span>
<span data-ttu-id="cb325-116">Имя FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="cb325-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="cb325-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb325-117">-ResourceGroupName</span></span>
<span data-ttu-id="cb325-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb325-118">The resource group name.</span></span>

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

### <span data-ttu-id="cb325-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb325-119">CommonParameters</span></span>
<span data-ttu-id="cb325-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb325-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb325-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb325-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb325-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb325-122">INPUTS</span></span>

### <span data-ttu-id="cb325-123">Нет</span><span class="sxs-lookup"><span data-stu-id="cb325-123">None</span></span>

## <span data-ttu-id="cb325-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb325-124">OUTPUTS</span></span>

### <span data-ttu-id="cb325-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="cb325-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="cb325-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cb325-126">NOTES</span></span>

## <span data-ttu-id="cb325-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb325-127">RELATED LINKS</span></span>

<span data-ttu-id="cb325-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="cb325-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>
