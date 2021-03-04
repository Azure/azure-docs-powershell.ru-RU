---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: 748dc399c68a299ef0d567fbd65ec7154061869c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954904"
---
# <span data-ttu-id="99aa5-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="99aa5-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="99aa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="99aa5-103">Добавляет продукт в группу.</span><span class="sxs-lookup"><span data-stu-id="99aa5-103">Adds a product to a group.</span></span>

## <span data-ttu-id="99aa5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="99aa5-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99aa5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99aa5-105">DESCRIPTION</span></span>
<span data-ttu-id="99aa5-106">Cmdlet **Add-AzApiManagementProductToGroup** добавляет продукт в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="99aa5-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="99aa5-107">Другими словами, этот cmdlet назначает группу продукту.</span><span class="sxs-lookup"><span data-stu-id="99aa5-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="99aa5-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="99aa5-108">EXAMPLES</span></span>

### <span data-ttu-id="99aa5-109">Пример 1. Добавление товара в группу</span><span class="sxs-lookup"><span data-stu-id="99aa5-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="99aa5-110">Эта команда добавляет продукт в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="99aa5-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="99aa5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99aa5-111">PARAMETERS</span></span>

### <span data-ttu-id="99aa5-112">-Контекст</span><span class="sxs-lookup"><span data-stu-id="99aa5-112">-Context</span></span>
<span data-ttu-id="99aa5-113">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="99aa5-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="99aa5-114">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="99aa5-114">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99aa5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99aa5-115">-DefaultProfile</span></span>
<span data-ttu-id="99aa5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99aa5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99aa5-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="99aa5-117">-GroupId</span></span>
<span data-ttu-id="99aa5-118">Определяет ИД группы.</span><span class="sxs-lookup"><span data-stu-id="99aa5-118">Specifies the group ID.</span></span>
<span data-ttu-id="99aa5-119">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="99aa5-119">This parameter is required.</span></span>

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

### <span data-ttu-id="99aa5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99aa5-120">-PassThru</span></span>
<span data-ttu-id="99aa5-121">passthru</span><span class="sxs-lookup"><span data-stu-id="99aa5-121">passthru</span></span>

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

### <span data-ttu-id="99aa5-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="99aa5-122">-ProductId</span></span>
<span data-ttu-id="99aa5-123">Определяет ИД продукта.</span><span class="sxs-lookup"><span data-stu-id="99aa5-123">Specifies the product ID.</span></span>
<span data-ttu-id="99aa5-124">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="99aa5-124">This parameter is required.</span></span>

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

### <span data-ttu-id="99aa5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99aa5-125">CommonParameters</span></span>
<span data-ttu-id="99aa5-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99aa5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99aa5-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99aa5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99aa5-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99aa5-128">INPUTS</span></span>

### <span data-ttu-id="99aa5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="99aa5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="99aa5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="99aa5-130">System.String</span></span>

### <span data-ttu-id="99aa5-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="99aa5-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="99aa5-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="99aa5-132">OUTPUTS</span></span>

### <span data-ttu-id="99aa5-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="99aa5-133">System.Boolean</span></span>

## <span data-ttu-id="99aa5-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="99aa5-134">NOTES</span></span>

## <span data-ttu-id="99aa5-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99aa5-135">RELATED LINKS</span></span>

[<span data-ttu-id="99aa5-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="99aa5-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


