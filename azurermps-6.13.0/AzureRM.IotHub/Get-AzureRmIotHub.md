---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 44cb5e9317c1806200a571dd6311e212e50a8c20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563000"
---
# <span data-ttu-id="31fd2-101">Get-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="31fd2-101">Get-AzureRmIotHub</span></span>

## <span data-ttu-id="31fd2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="31fd2-103">Получение сведений о IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="31fd2-103">Gets information about the IotHubs in a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31fd2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31fd2-104">SYNTAX</span></span>

### <span data-ttu-id="31fd2-105">ListIotHubsByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31fd2-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31fd2-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="31fd2-106">GetIotHubByName</span></span>
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31fd2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31fd2-107">DESCRIPTION</span></span>
<span data-ttu-id="31fd2-108">Получение сведений о IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="31fd2-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="31fd2-109">Вы можете просмотреть все экземпляры IotHub в подписке или отфильтровать результаты по группе ресурсов или определенному имени IotHub.</span><span class="sxs-lookup"><span data-stu-id="31fd2-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="31fd2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31fd2-110">EXAMPLES</span></span>

### <span data-ttu-id="31fd2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="31fd2-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHub
```

<span data-ttu-id="31fd2-112">Получает все IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="31fd2-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="31fd2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="31fd2-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="31fd2-114">Получает все IotHubs в подписке, относящиеся к группе ресурсов "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="31fd2-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="31fd2-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="31fd2-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="31fd2-116">Получает сведения о IotHub с именем "myiothub".</span><span class="sxs-lookup"><span data-stu-id="31fd2-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="31fd2-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31fd2-117">PARAMETERS</span></span>

### <span data-ttu-id="31fd2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31fd2-118">-DefaultProfile</span></span>
<span data-ttu-id="31fd2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="31fd2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31fd2-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31fd2-120">-Name</span></span>
<span data-ttu-id="31fd2-121">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="31fd2-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31fd2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31fd2-122">-ResourceGroupName</span></span>
<span data-ttu-id="31fd2-123">Имя элемента ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="31fd2-123">Name of the ResourceGroup</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31fd2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31fd2-124">CommonParameters</span></span>
<span data-ttu-id="31fd2-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31fd2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31fd2-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31fd2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31fd2-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31fd2-127">INPUTS</span></span>

### <span data-ttu-id="31fd2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="31fd2-128">System.String</span></span>

## <span data-ttu-id="31fd2-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31fd2-129">OUTPUTS</span></span>

### <span data-ttu-id="31fd2-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="31fd2-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="31fd2-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="31fd2-131">NOTES</span></span>

## <span data-ttu-id="31fd2-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31fd2-132">RELATED LINKS</span></span>
