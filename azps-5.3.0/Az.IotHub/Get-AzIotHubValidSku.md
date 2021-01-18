---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: e0f178c10fa74d8fa230472397d7bcc835f98bf4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518602"
---
# <span data-ttu-id="1af07-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="1af07-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="1af07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1af07-102">SYNOPSIS</span></span>
<span data-ttu-id="1af07-103">Получает все допустимые skus, к которые может перейти этот IotHub.</span><span class="sxs-lookup"><span data-stu-id="1af07-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="1af07-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1af07-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1af07-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1af07-105">DESCRIPTION</span></span>
<span data-ttu-id="1af07-106">Получает все действительные skus, к которые может перейти этот IotHub.</span><span class="sxs-lookup"><span data-stu-id="1af07-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="1af07-107">IotHub не может перейти между бесплатными и платными skus и наоборот.</span><span class="sxs-lookup"><span data-stu-id="1af07-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="1af07-108">Для этого вам придется удалить и заново создать iothub.</span><span class="sxs-lookup"><span data-stu-id="1af07-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="1af07-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1af07-109">EXAMPLES</span></span>

### <span data-ttu-id="1af07-110">Пример 1. Получить действительные skus</span><span class="sxs-lookup"><span data-stu-id="1af07-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="1af07-111">Получает список всех skus для IotHub с именем myiothub.</span><span class="sxs-lookup"><span data-stu-id="1af07-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="1af07-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1af07-112">PARAMETERS</span></span>

### <span data-ttu-id="1af07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af07-113">-DefaultProfile</span></span>
<span data-ttu-id="1af07-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1af07-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1af07-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1af07-115">-Name</span></span>
<span data-ttu-id="1af07-116">Имя концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="1af07-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="1af07-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af07-117">-ResourceGroupName</span></span>
<span data-ttu-id="1af07-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1af07-118">Resource Group Name</span></span>

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

### <span data-ttu-id="1af07-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af07-119">CommonParameters</span></span>
<span data-ttu-id="1af07-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1af07-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af07-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1af07-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af07-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1af07-122">INPUTS</span></span>

### <span data-ttu-id="1af07-123">System.String</span><span class="sxs-lookup"><span data-stu-id="1af07-123">System.String</span></span>

## <span data-ttu-id="1af07-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1af07-124">OUTPUTS</span></span>

### <span data-ttu-id="1af07-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="1af07-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="1af07-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1af07-126">NOTES</span></span>

## <span data-ttu-id="1af07-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1af07-127">RELATED LINKS</span></span>
