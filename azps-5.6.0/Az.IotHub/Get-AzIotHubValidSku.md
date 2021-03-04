---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: b51c41ddd36d19afedd0091be9b0a00bb447faaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964616"
---
# <span data-ttu-id="7837f-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="7837f-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="7837f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7837f-102">SYNOPSIS</span></span>
<span data-ttu-id="7837f-103">Получает все допустимые skus, к которые может перейти этот IotHub.</span><span class="sxs-lookup"><span data-stu-id="7837f-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="7837f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7837f-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7837f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7837f-105">DESCRIPTION</span></span>
<span data-ttu-id="7837f-106">Возвращает все действительные skus, к которые может перейти этот IotHub.</span><span class="sxs-lookup"><span data-stu-id="7837f-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="7837f-107">IotHub не может переход между бесплатными и платными skus и наоборот.</span><span class="sxs-lookup"><span data-stu-id="7837f-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="7837f-108">Для этого вам придется удалить и заново создать iothub.</span><span class="sxs-lookup"><span data-stu-id="7837f-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="7837f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7837f-109">EXAMPLES</span></span>

### <span data-ttu-id="7837f-110">Пример 1. Получить действительные skus</span><span class="sxs-lookup"><span data-stu-id="7837f-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="7837f-111">Получает список всех skus для IotHub под названием "myiothub"</span><span class="sxs-lookup"><span data-stu-id="7837f-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="7837f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7837f-112">PARAMETERS</span></span>

### <span data-ttu-id="7837f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7837f-113">-DefaultProfile</span></span>
<span data-ttu-id="7837f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7837f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7837f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7837f-115">-Name</span></span>
<span data-ttu-id="7837f-116">Имя концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="7837f-116">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7837f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7837f-117">-ResourceGroupName</span></span>
<span data-ttu-id="7837f-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7837f-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7837f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7837f-119">CommonParameters</span></span>
<span data-ttu-id="7837f-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7837f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7837f-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7837f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7837f-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7837f-122">INPUTS</span></span>

### <span data-ttu-id="7837f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7837f-123">System.String</span></span>

## <span data-ttu-id="7837f-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7837f-124">OUTPUTS</span></span>

### <span data-ttu-id="7837f-125">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="7837f-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="7837f-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7837f-126">NOTES</span></span>

## <span data-ttu-id="7837f-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7837f-127">RELATED LINKS</span></span>
