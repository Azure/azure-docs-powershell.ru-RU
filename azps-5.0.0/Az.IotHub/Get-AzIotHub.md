---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 0656726757584bf923d6ecaa7642aa67ff46596a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247771"
---
# <span data-ttu-id="b56d9-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="b56d9-101">Get-AzIotHub</span></span>

## <span data-ttu-id="b56d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b56d9-102">SYNOPSIS</span></span>
<span data-ttu-id="b56d9-103">Получение сведений о IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="b56d9-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="b56d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b56d9-104">SYNTAX</span></span>

### <span data-ttu-id="b56d9-105">ListIotHubsByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b56d9-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b56d9-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="b56d9-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b56d9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b56d9-107">DESCRIPTION</span></span>
<span data-ttu-id="b56d9-108">Получение сведений о IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="b56d9-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="b56d9-109">Вы можете просмотреть все экземпляры IotHub в подписке или отфильтровать результаты по группе ресурсов или определенному имени IotHub.</span><span class="sxs-lookup"><span data-stu-id="b56d9-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="b56d9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b56d9-110">EXAMPLES</span></span>

### <span data-ttu-id="b56d9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b56d9-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="b56d9-112">Получает все IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="b56d9-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="b56d9-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b56d9-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="b56d9-114">Получает все IotHubs в подписке, относящиеся к группе ресурсов "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="b56d9-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="b56d9-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b56d9-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b56d9-116">Получает сведения о IotHub с именем "myiothub".</span><span class="sxs-lookup"><span data-stu-id="b56d9-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="b56d9-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b56d9-117">PARAMETERS</span></span>

### <span data-ttu-id="b56d9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b56d9-118">-DefaultProfile</span></span>
<span data-ttu-id="b56d9-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b56d9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b56d9-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b56d9-120">-Name</span></span>
<span data-ttu-id="b56d9-121">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="b56d9-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="b56d9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b56d9-122">-ResourceGroupName</span></span>
<span data-ttu-id="b56d9-123">Имя элемента ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b56d9-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="b56d9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b56d9-124">CommonParameters</span></span>
<span data-ttu-id="b56d9-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b56d9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b56d9-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b56d9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b56d9-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b56d9-127">INPUTS</span></span>

### <span data-ttu-id="b56d9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b56d9-128">System.String</span></span>

## <span data-ttu-id="b56d9-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b56d9-129">OUTPUTS</span></span>

### <span data-ttu-id="b56d9-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b56d9-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="b56d9-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b56d9-131">NOTES</span></span>

## <span data-ttu-id="b56d9-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b56d9-132">RELATED LINKS</span></span>