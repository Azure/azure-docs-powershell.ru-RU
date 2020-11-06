---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 890180c024a004652406e04530a7e3291def13ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569388"
---
# <span data-ttu-id="d23ac-101">Get-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="d23ac-101">Get-AzureRmIotHub</span></span>

## <span data-ttu-id="d23ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d23ac-102">SYNOPSIS</span></span>
<span data-ttu-id="d23ac-103">Получение сведений о IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="d23ac-103">Gets information about the IotHubs in a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d23ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d23ac-104">SYNTAX</span></span>

### <span data-ttu-id="d23ac-105">ListIotHubsByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d23ac-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d23ac-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="d23ac-106">GetIotHubByName</span></span>
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d23ac-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d23ac-107">DESCRIPTION</span></span>
<span data-ttu-id="d23ac-108">Получение сведений о IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="d23ac-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="d23ac-109">Вы можете просмотреть все экземпляры IotHub в подписке или отфильтровать результаты по группе ресурсов или определенному имени IotHub.</span><span class="sxs-lookup"><span data-stu-id="d23ac-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="d23ac-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d23ac-110">EXAMPLES</span></span>

### <span data-ttu-id="d23ac-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d23ac-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHub
```

<span data-ttu-id="d23ac-112">Получает все IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="d23ac-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="d23ac-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d23ac-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="d23ac-114">Получает все IotHubs в подписке, относящиеся к группе ресурсов "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="d23ac-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="d23ac-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d23ac-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="d23ac-116">Получает сведения о IotHub с именем "myiothub".</span><span class="sxs-lookup"><span data-stu-id="d23ac-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="d23ac-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d23ac-117">PARAMETERS</span></span>

### <span data-ttu-id="d23ac-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d23ac-118">-Name</span></span>
<span data-ttu-id="d23ac-119">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="d23ac-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="d23ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d23ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="d23ac-121">Имя элемента ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d23ac-121">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="d23ac-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d23ac-122">-DefaultProfile</span></span>
<span data-ttu-id="d23ac-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d23ac-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d23ac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d23ac-124">CommonParameters</span></span>
<span data-ttu-id="d23ac-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d23ac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d23ac-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d23ac-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d23ac-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d23ac-127">INPUTS</span></span>

### <span data-ttu-id="d23ac-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d23ac-128">System.String</span></span>

## <span data-ttu-id="d23ac-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d23ac-129">OUTPUTS</span></span>

### <span data-ttu-id="d23ac-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d23ac-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="d23ac-131">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="d23ac-131">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="d23ac-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="d23ac-132">NOTES</span></span>

## <span data-ttu-id="d23ac-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d23ac-133">RELATED LINKS</span></span>

