---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: 05f3ac10171c9135b59b9fb6894f5b5fbf670de0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960899"
---
# <span data-ttu-id="93dc2-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="93dc2-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="93dc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="93dc2-103">Удаляет продукт из группы.</span><span class="sxs-lookup"><span data-stu-id="93dc2-103">Removes a product from a group.</span></span>

## <span data-ttu-id="93dc2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="93dc2-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93dc2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93dc2-105">DESCRIPTION</span></span>
<span data-ttu-id="93dc2-106">При этом из **существующей** группы удаляется продукт из существующей группы.</span><span class="sxs-lookup"><span data-stu-id="93dc2-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="93dc2-107">Другими словами, этот cmdlet удаляет назначение группы из продукта.</span><span class="sxs-lookup"><span data-stu-id="93dc2-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="93dc2-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="93dc2-108">EXAMPLES</span></span>

### <span data-ttu-id="93dc2-109">Пример 1. Удаление продукта из группы</span><span class="sxs-lookup"><span data-stu-id="93dc2-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="93dc2-110">Эта команда удаляет продукт из существующей группы.</span><span class="sxs-lookup"><span data-stu-id="93dc2-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="93dc2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93dc2-111">PARAMETERS</span></span>

### <span data-ttu-id="93dc2-112">-Контекст</span><span class="sxs-lookup"><span data-stu-id="93dc2-112">-Context</span></span>
<span data-ttu-id="93dc2-113">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="93dc2-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="93dc2-114">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="93dc2-114">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93dc2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93dc2-115">-DefaultProfile</span></span>
<span data-ttu-id="93dc2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93dc2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93dc2-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="93dc2-117">-GroupId</span></span>
<span data-ttu-id="93dc2-118">Определяет ИД группы.</span><span class="sxs-lookup"><span data-stu-id="93dc2-118">Specifies the group ID.</span></span>
<span data-ttu-id="93dc2-119">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="93dc2-119">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93dc2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93dc2-120">-PassThru</span></span>
<span data-ttu-id="93dc2-121">Указывает на то, что этот $True возвращает значение, если он успешно или $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="93dc2-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93dc2-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="93dc2-122">-ProductId</span></span>
<span data-ttu-id="93dc2-123">Определяет ИД продукта.</span><span class="sxs-lookup"><span data-stu-id="93dc2-123">Specifies the product ID.</span></span>
<span data-ttu-id="93dc2-124">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="93dc2-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93dc2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93dc2-125">CommonParameters</span></span>
<span data-ttu-id="93dc2-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93dc2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93dc2-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93dc2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93dc2-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93dc2-128">INPUTS</span></span>

### <span data-ttu-id="93dc2-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="93dc2-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="93dc2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="93dc2-130">System.String</span></span>

### <span data-ttu-id="93dc2-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="93dc2-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="93dc2-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="93dc2-132">OUTPUTS</span></span>

### <span data-ttu-id="93dc2-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93dc2-133">System.Boolean</span></span>

## <span data-ttu-id="93dc2-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="93dc2-134">NOTES</span></span>

## <span data-ttu-id="93dc2-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93dc2-135">RELATED LINKS</span></span>

[<span data-ttu-id="93dc2-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="93dc2-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


