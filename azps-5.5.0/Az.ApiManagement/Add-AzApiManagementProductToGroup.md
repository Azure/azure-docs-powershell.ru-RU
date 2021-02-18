---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: a92387392c540c75cfa96ecaf4c4acf026ade9f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239909"
---
# <span data-ttu-id="b3514-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="b3514-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="b3514-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3514-102">SYNOPSIS</span></span>
<span data-ttu-id="b3514-103">Добавляет продукт в группу.</span><span class="sxs-lookup"><span data-stu-id="b3514-103">Adds a product to a group.</span></span>

## <span data-ttu-id="b3514-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b3514-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3514-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3514-105">DESCRIPTION</span></span>
<span data-ttu-id="b3514-106">Cmdlet **Add-AzApiManagementProductToGroup** добавляет продукт в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="b3514-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="b3514-107">Другими словами, этот cmdlet назначает группу продукту.</span><span class="sxs-lookup"><span data-stu-id="b3514-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="b3514-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b3514-108">EXAMPLES</span></span>

### <span data-ttu-id="b3514-109">Пример 1. Добавление товара в группу</span><span class="sxs-lookup"><span data-stu-id="b3514-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="b3514-110">Эта команда добавляет продукт в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="b3514-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="b3514-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3514-111">PARAMETERS</span></span>

### <span data-ttu-id="b3514-112">-Контекст</span><span class="sxs-lookup"><span data-stu-id="b3514-112">-Context</span></span>
<span data-ttu-id="b3514-113">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="b3514-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="b3514-114">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="b3514-114">This parameter is required.</span></span>

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

### <span data-ttu-id="b3514-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3514-115">-DefaultProfile</span></span>
<span data-ttu-id="b3514-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3514-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3514-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="b3514-117">-GroupId</span></span>
<span data-ttu-id="b3514-118">Определяет ИД группы.</span><span class="sxs-lookup"><span data-stu-id="b3514-118">Specifies the group ID.</span></span>
<span data-ttu-id="b3514-119">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="b3514-119">This parameter is required.</span></span>

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

### <span data-ttu-id="b3514-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3514-120">-PassThru</span></span>
<span data-ttu-id="b3514-121">passthru</span><span class="sxs-lookup"><span data-stu-id="b3514-121">passthru</span></span>

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

### <span data-ttu-id="b3514-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="b3514-122">-ProductId</span></span>
<span data-ttu-id="b3514-123">Определяет ИД продукта.</span><span class="sxs-lookup"><span data-stu-id="b3514-123">Specifies the product ID.</span></span>
<span data-ttu-id="b3514-124">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="b3514-124">This parameter is required.</span></span>

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

### <span data-ttu-id="b3514-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3514-125">CommonParameters</span></span>
<span data-ttu-id="b3514-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3514-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3514-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3514-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3514-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3514-128">INPUTS</span></span>

### <span data-ttu-id="b3514-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b3514-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b3514-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b3514-130">System.String</span></span>

### <span data-ttu-id="b3514-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b3514-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b3514-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b3514-132">OUTPUTS</span></span>

### <span data-ttu-id="b3514-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3514-133">System.Boolean</span></span>

## <span data-ttu-id="b3514-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b3514-134">NOTES</span></span>

## <span data-ttu-id="b3514-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3514-135">RELATED LINKS</span></span>

[<span data-ttu-id="b3514-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="b3514-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


