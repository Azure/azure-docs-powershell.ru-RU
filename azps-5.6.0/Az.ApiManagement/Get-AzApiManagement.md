---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: a4a6cf459c253c26f5d550492f8b756d59fcdf44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994619"
---
# <span data-ttu-id="a83ab-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a83ab-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="a83ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a83ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a83ab-103">Возвращает список или описание конкретной службы управления API.</span><span class="sxs-lookup"><span data-stu-id="a83ab-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="a83ab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a83ab-104">SYNTAX</span></span>

### <span data-ttu-id="a83ab-105">GetBySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a83ab-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a83ab-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a83ab-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a83ab-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="a83ab-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a83ab-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a83ab-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a83ab-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a83ab-109">DESCRIPTION</span></span>
<span data-ttu-id="a83ab-110">Для получения списка всех служб управления API в рамках подписки, указанной группы ресурсов или определенной системы управления API, можно получить список управляющих служб **Get-AzApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="a83ab-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="a83ab-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a83ab-111">EXAMPLES</span></span>

### <span data-ttu-id="a83ab-112">Пример 1. Получить все службы управления API</span><span class="sxs-lookup"><span data-stu-id="a83ab-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="a83ab-113">Эта команда получает все службы управления API в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="a83ab-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="a83ab-114">Пример 2. Получить все службы управления API по определенному имени</span><span class="sxs-lookup"><span data-stu-id="a83ab-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="a83ab-115">Эта команда получает все службы управления API по имени.</span><span class="sxs-lookup"><span data-stu-id="a83ab-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="a83ab-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a83ab-116">PARAMETERS</span></span>

### <span data-ttu-id="a83ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a83ab-117">-DefaultProfile</span></span>
<span data-ttu-id="a83ab-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a83ab-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a83ab-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a83ab-119">-Name</span></span>
<span data-ttu-id="a83ab-120">Указывает имя службы управления API.</span><span class="sxs-lookup"><span data-stu-id="a83ab-120">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a83ab-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a83ab-121">-ResourceGroupName</span></span>
<span data-ttu-id="a83ab-122">Имя группы ресурсов, под которой этот cmdlet получает службу управления API.</span><span class="sxs-lookup"><span data-stu-id="a83ab-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a83ab-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a83ab-123">-ResourceId</span></span>
<span data-ttu-id="a83ab-124">Arm ResourceId службы управления API.</span><span class="sxs-lookup"><span data-stu-id="a83ab-124">Arm ResourceId of the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a83ab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a83ab-125">CommonParameters</span></span>
<span data-ttu-id="a83ab-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a83ab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a83ab-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a83ab-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a83ab-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a83ab-128">INPUTS</span></span>

### <span data-ttu-id="a83ab-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a83ab-129">System.String</span></span>

## <span data-ttu-id="a83ab-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a83ab-130">OUTPUTS</span></span>

### <span data-ttu-id="a83ab-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="a83ab-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="a83ab-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a83ab-132">NOTES</span></span>

## <span data-ttu-id="a83ab-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a83ab-133">RELATED LINKS</span></span>

[<span data-ttu-id="a83ab-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a83ab-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="a83ab-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a83ab-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="a83ab-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a83ab-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="a83ab-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a83ab-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


