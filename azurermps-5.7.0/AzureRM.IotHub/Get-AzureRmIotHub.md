---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 80b629fe3d5ff5e028b73b22af95243849ecede7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732642"
---
# <span data-ttu-id="ee98c-101">Get-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="ee98c-101">Get-AzureRmIotHub</span></span>

## <span data-ttu-id="ee98c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee98c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee98c-103">Получение сведений о IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="ee98c-103">Gets information about the IotHubs in a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee98c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee98c-104">SYNTAX</span></span>

### <span data-ttu-id="ee98c-105">ListIotHubsByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee98c-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee98c-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="ee98c-106">GetIotHubByName</span></span>
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee98c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee98c-107">DESCRIPTION</span></span>
<span data-ttu-id="ee98c-108">Получение сведений о IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="ee98c-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="ee98c-109">Вы можете просмотреть все экземпляры IotHub в подписке или отфильтровать результаты по группе ресурсов или определенному имени IotHub.</span><span class="sxs-lookup"><span data-stu-id="ee98c-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="ee98c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee98c-110">EXAMPLES</span></span>

### <span data-ttu-id="ee98c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee98c-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHub
```

<span data-ttu-id="ee98c-112">Получает все IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="ee98c-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="ee98c-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ee98c-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="ee98c-114">Получает все IotHubs в подписке, относящиеся к группе ресурсов "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="ee98c-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="ee98c-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ee98c-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ee98c-116">Получает сведения о IotHub с именем "myiothub".</span><span class="sxs-lookup"><span data-stu-id="ee98c-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="ee98c-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee98c-117">PARAMETERS</span></span>

### <span data-ttu-id="ee98c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee98c-118">-DefaultProfile</span></span>
<span data-ttu-id="ee98c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ee98c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee98c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ee98c-120">-Name</span></span>
<span data-ttu-id="ee98c-121">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="ee98c-121">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee98c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee98c-122">-ResourceGroupName</span></span>
<span data-ttu-id="ee98c-123">Имя элемента ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ee98c-123">Name of the ResourceGroup</span></span>

```yaml
Type: String
Parameter Sets: ListIotHubsByResourceGroup
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee98c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee98c-124">CommonParameters</span></span>
<span data-ttu-id="ee98c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee98c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee98c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee98c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee98c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee98c-127">INPUTS</span></span>

### <span data-ttu-id="ee98c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ee98c-128">System.String</span></span>

## <span data-ttu-id="ee98c-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee98c-129">OUTPUTS</span></span>

### <span data-ttu-id="ee98c-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ee98c-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="ee98c-131">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="ee98c-131">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="ee98c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee98c-132">NOTES</span></span>

## <span data-ttu-id="ee98c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee98c-133">RELATED LINKS</span></span>

