---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 60d6263d3fb074cf4795379ae28f1824dc81a4c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720901"
---
# <span data-ttu-id="c4254-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="c4254-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="c4254-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4254-102">SYNOPSIS</span></span>
<span data-ttu-id="c4254-103">Получение политики WAF</span><span class="sxs-lookup"><span data-stu-id="c4254-103">Get WAF policy</span></span>

## <span data-ttu-id="c4254-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4254-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4254-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4254-105">DESCRIPTION</span></span>
<span data-ttu-id="c4254-106">Параметр **Get-AzFrontDoorWafPolicy** CMDLETGET получает WAF политику в группе ресурсов в рамках текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="c4254-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="c4254-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4254-107">EXAMPLES</span></span>

### <span data-ttu-id="c4254-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c4254-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="c4254-109">Получение WAF политики с именем $policyName в $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4254-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="c4254-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c4254-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="c4254-111">Получение всех WAF политики в $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4254-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="c4254-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4254-112">PARAMETERS</span></span>

### <span data-ttu-id="c4254-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4254-113">-DefaultProfile</span></span>
<span data-ttu-id="c4254-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4254-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4254-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c4254-115">-Name</span></span>
<span data-ttu-id="c4254-116">FireWallPolicy имя.</span><span class="sxs-lookup"><span data-stu-id="c4254-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="c4254-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4254-117">-ResourceGroupName</span></span>
<span data-ttu-id="c4254-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4254-118">The resource group name.</span></span>

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

### <span data-ttu-id="c4254-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4254-119">CommonParameters</span></span>
<span data-ttu-id="c4254-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4254-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4254-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4254-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4254-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4254-122">INPUTS</span></span>

### <span data-ttu-id="c4254-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="c4254-123">None</span></span>

## <span data-ttu-id="c4254-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4254-124">OUTPUTS</span></span>

### <span data-ttu-id="c4254-125">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="c4254-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="c4254-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4254-126">NOTES</span></span>

## <span data-ttu-id="c4254-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4254-127">RELATED LINKS</span></span>

<span data-ttu-id="c4254-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="c4254-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>
