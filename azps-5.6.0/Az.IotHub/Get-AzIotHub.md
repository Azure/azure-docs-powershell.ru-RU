---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 6937d79d6f60c053238075713f5d58432124e7e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988168"
---
# <span data-ttu-id="de48e-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="de48e-101">Get-AzIotHub</span></span>

## <span data-ttu-id="de48e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de48e-102">SYNOPSIS</span></span>
<span data-ttu-id="de48e-103">Получает сведения об IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="de48e-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="de48e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="de48e-104">SYNTAX</span></span>

### <span data-ttu-id="de48e-105">ListIotHubsByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="de48e-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de48e-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="de48e-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de48e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de48e-107">DESCRIPTION</span></span>
<span data-ttu-id="de48e-108">Получает сведения об IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="de48e-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="de48e-109">Вы можете просмотреть все экземпляры IotHub в подписке или отфильтровать результаты по группе ресурсов или определенному имени IotHub.</span><span class="sxs-lookup"><span data-stu-id="de48e-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="de48e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="de48e-110">EXAMPLES</span></span>

### <span data-ttu-id="de48e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="de48e-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="de48e-112">Получает все IotHubs в подписке.</span><span class="sxs-lookup"><span data-stu-id="de48e-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="de48e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="de48e-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="de48e-114">Получает все IotHubs в подписке, принадлежащие группе ресурсов "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="de48e-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="de48e-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="de48e-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="de48e-116">Получает сведения о IotHub с именем myiothub.</span><span class="sxs-lookup"><span data-stu-id="de48e-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="de48e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de48e-117">PARAMETERS</span></span>

### <span data-ttu-id="de48e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de48e-118">-DefaultProfile</span></span>
<span data-ttu-id="de48e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="de48e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de48e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="de48e-120">-Name</span></span>
<span data-ttu-id="de48e-121">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="de48e-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="de48e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de48e-122">-ResourceGroupName</span></span>
<span data-ttu-id="de48e-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="de48e-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="de48e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de48e-124">CommonParameters</span></span>
<span data-ttu-id="de48e-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de48e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de48e-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de48e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de48e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de48e-127">INPUTS</span></span>

### <span data-ttu-id="de48e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="de48e-128">System.String</span></span>

## <span data-ttu-id="de48e-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="de48e-129">OUTPUTS</span></span>

### <span data-ttu-id="de48e-130">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="de48e-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="de48e-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="de48e-131">NOTES</span></span>

## <span data-ttu-id="de48e-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de48e-132">RELATED LINKS</span></span>
