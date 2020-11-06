---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 283bc1a14404c842da0ed99e43596984b1559299
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566457"
---
# <span data-ttu-id="174a8-101">Get-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="174a8-101">Get-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="174a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="174a8-102">SYNOPSIS</span></span>
<span data-ttu-id="174a8-103">Получение политики WAF</span><span class="sxs-lookup"><span data-stu-id="174a8-103">Get WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="174a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="174a8-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="174a8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="174a8-105">DESCRIPTION</span></span>
<span data-ttu-id="174a8-106">Параметр **Get-AzureRmFrontDoorFireWallPolicy** CMDLETGET получает WAF политику в группе ресурсов в рамках текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="174a8-106">The **Get-AzureRmFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="174a8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="174a8-107">EXAMPLES</span></span>

### <span data-ttu-id="174a8-108">Пример 1: получение политики WAF с именем $Name в $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="174a8-108">Example 1: Get a WAF policy called $Name in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="174a8-109">Получение WAF политики с именем $Name в $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="174a8-109">Get a WAF policy called $Name in $resourceGroup</span></span>

### <span data-ttu-id="174a8-110">Пример 2: получение всей политики WAF в $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="174a8-110">Example 2: Get all WAF policy in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name1}
Name               : {Name1}
Type               :

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name2}
Name               : {Name2}
Type               :
```

<span data-ttu-id="174a8-111">Получение всех WAF политики в $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="174a8-111">Get all WAF policy in $resourceGroup</span></span>

## <span data-ttu-id="174a8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="174a8-112">PARAMETERS</span></span>

### <span data-ttu-id="174a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="174a8-113">-DefaultProfile</span></span>
<span data-ttu-id="174a8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="174a8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="174a8-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="174a8-115">-Name</span></span>
<span data-ttu-id="174a8-116">FireWallPolicy имя.</span><span class="sxs-lookup"><span data-stu-id="174a8-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="174a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="174a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="174a8-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="174a8-118">The resource group name.</span></span>

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

### <span data-ttu-id="174a8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="174a8-119">CommonParameters</span></span>
<span data-ttu-id="174a8-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="174a8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="174a8-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="174a8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="174a8-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="174a8-122">INPUTS</span></span>

### <span data-ttu-id="174a8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="174a8-123">System.String</span></span>

## <span data-ttu-id="174a8-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="174a8-124">OUTPUTS</span></span>

### <span data-ttu-id="174a8-125">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="174a8-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="174a8-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="174a8-126">NOTES</span></span>

## <span data-ttu-id="174a8-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="174a8-127">RELATED LINKS</span></span>

<span data-ttu-id="174a8-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="174a8-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span></span>
