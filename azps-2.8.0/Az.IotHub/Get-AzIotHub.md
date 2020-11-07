---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: d544de6badaa6ce64e8165696cc7dff2a595d75e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720757"
---
# <span data-ttu-id="8298a-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="8298a-101">Get-AzIotHub</span></span>

## <span data-ttu-id="8298a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8298a-102">SYNOPSIS</span></span>
<span data-ttu-id="8298a-103">Получение сведений о IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="8298a-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="8298a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8298a-104">SYNTAX</span></span>

### <span data-ttu-id="8298a-105">ListIotHubsByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8298a-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8298a-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="8298a-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8298a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8298a-107">DESCRIPTION</span></span>
<span data-ttu-id="8298a-108">Получение сведений о IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="8298a-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="8298a-109">Вы можете просмотреть все экземпляры IotHub в подписке или отфильтровать результаты по группе ресурсов или определенному имени IotHub.</span><span class="sxs-lookup"><span data-stu-id="8298a-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="8298a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8298a-110">EXAMPLES</span></span>

### <span data-ttu-id="8298a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8298a-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="8298a-112">Получает все IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="8298a-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="8298a-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8298a-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="8298a-114">Получает все IotHubs в подписке, относящиеся к группе ресурсов "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="8298a-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="8298a-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8298a-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="8298a-116">Получает сведения о IotHub с именем "myiothub".</span><span class="sxs-lookup"><span data-stu-id="8298a-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="8298a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8298a-117">PARAMETERS</span></span>

### <span data-ttu-id="8298a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8298a-118">-DefaultProfile</span></span>
<span data-ttu-id="8298a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8298a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8298a-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8298a-120">-Name</span></span>
<span data-ttu-id="8298a-121">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="8298a-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="8298a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8298a-122">-ResourceGroupName</span></span>
<span data-ttu-id="8298a-123">Имя элемента ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8298a-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="8298a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8298a-124">CommonParameters</span></span>
<span data-ttu-id="8298a-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8298a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8298a-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8298a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8298a-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8298a-127">INPUTS</span></span>

### <span data-ttu-id="8298a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8298a-128">System.String</span></span>

## <span data-ttu-id="8298a-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8298a-129">OUTPUTS</span></span>

### <span data-ttu-id="8298a-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8298a-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="8298a-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="8298a-131">NOTES</span></span>

## <span data-ttu-id="8298a-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8298a-132">RELATED LINKS</span></span>
