---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: c95fe4a977c70964cf8b4dab86985d79315d3141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008648"
---
# <span data-ttu-id="afc7f-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="afc7f-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="afc7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afc7f-102">SYNOPSIS</span></span>
<span data-ttu-id="afc7f-103">Получает управляемые приложения</span><span class="sxs-lookup"><span data-stu-id="afc7f-103">Gets managed applications</span></span>

## <span data-ttu-id="afc7f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="afc7f-104">SYNTAX</span></span>

### <span data-ttu-id="afc7f-105">GetBySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="afc7f-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="afc7f-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="afc7f-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afc7f-107">GetById</span><span class="sxs-lookup"><span data-stu-id="afc7f-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afc7f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afc7f-108">DESCRIPTION</span></span>
<span data-ttu-id="afc7f-109">Управляемые **приложения получает cmdlet Get-AzManagedApplication**</span><span class="sxs-lookup"><span data-stu-id="afc7f-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="afc7f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="afc7f-110">EXAMPLES</span></span>

### <span data-ttu-id="afc7f-111">Пример 1. Получение всех управляемых приложений в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="afc7f-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="afc7f-112">Эта команда получает управляемые приложения в группе ресурсов MyRG.</span><span class="sxs-lookup"><span data-stu-id="afc7f-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="afc7f-113">Пример 2. Получение всех управляемых приложений</span><span class="sxs-lookup"><span data-stu-id="afc7f-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="afc7f-114">Эта команда для получения всех управляемых приложений в рамках текущей подписки</span><span class="sxs-lookup"><span data-stu-id="afc7f-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="afc7f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afc7f-115">PARAMETERS</span></span>

### <span data-ttu-id="afc7f-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="afc7f-116">-ApiVersion</span></span>
<span data-ttu-id="afc7f-117">Указывает версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="afc7f-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="afc7f-118">Если он не задан, версия API будет автоматически определена как наиболее последняя из доступных.</span><span class="sxs-lookup"><span data-stu-id="afc7f-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="afc7f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afc7f-119">-DefaultProfile</span></span>
<span data-ttu-id="afc7f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="afc7f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afc7f-121">-Id</span><span class="sxs-lookup"><span data-stu-id="afc7f-121">-Id</span></span>
<span data-ttu-id="afc7f-122">Полностью управляемый ИД приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="afc7f-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="afc7f-123">Например, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="afc7f-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afc7f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="afc7f-124">-Name</span></span>
<span data-ttu-id="afc7f-125">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="afc7f-125">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afc7f-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="afc7f-126">-Pre</span></span>
<span data-ttu-id="afc7f-127">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="afc7f-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afc7f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afc7f-128">-ResourceGroupName</span></span>
<span data-ttu-id="afc7f-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="afc7f-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afc7f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afc7f-130">CommonParameters</span></span>
<span data-ttu-id="afc7f-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afc7f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afc7f-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afc7f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afc7f-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afc7f-133">INPUTS</span></span>

### <span data-ttu-id="afc7f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="afc7f-134">System.String</span></span>

## <span data-ttu-id="afc7f-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="afc7f-135">OUTPUTS</span></span>

### <span data-ttu-id="afc7f-136">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="afc7f-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="afc7f-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="afc7f-137">NOTES</span></span>

## <span data-ttu-id="afc7f-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="afc7f-138">RELATED LINKS</span></span>
