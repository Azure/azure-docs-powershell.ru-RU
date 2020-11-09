---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: a2afd2d5296912606363eddab49e0e3d6b371538
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318734"
---
# <span data-ttu-id="c429b-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="c429b-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="c429b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c429b-102">SYNOPSIS</span></span>
<span data-ttu-id="c429b-103">Удаление продукта из группы.</span><span class="sxs-lookup"><span data-stu-id="c429b-103">Removes a product from a group.</span></span>

## <span data-ttu-id="c429b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c429b-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c429b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c429b-105">DESCRIPTION</span></span>
<span data-ttu-id="c429b-106">Командлет **Remove-AzApiManagementProductFromGroup** удаляет продукт из существующей группы.</span><span class="sxs-lookup"><span data-stu-id="c429b-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="c429b-107">Другими словами, этот командлет удаляет назначение групп из продукта.</span><span class="sxs-lookup"><span data-stu-id="c429b-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="c429b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c429b-108">EXAMPLES</span></span>

### <span data-ttu-id="c429b-109">Пример 1: удаление продукта из группы</span><span class="sxs-lookup"><span data-stu-id="c429b-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="c429b-110">Эта команда удаляет продукт из существующей группы.</span><span class="sxs-lookup"><span data-stu-id="c429b-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="c429b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c429b-111">PARAMETERS</span></span>

### <span data-ttu-id="c429b-112">-Context</span><span class="sxs-lookup"><span data-stu-id="c429b-112">-Context</span></span>
<span data-ttu-id="c429b-113">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c429b-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="c429b-114">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c429b-114">This parameter is required.</span></span>

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

### <span data-ttu-id="c429b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c429b-115">-DefaultProfile</span></span>
<span data-ttu-id="c429b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c429b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c429b-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="c429b-117">-GroupId</span></span>
<span data-ttu-id="c429b-118">Указывает код группы.</span><span class="sxs-lookup"><span data-stu-id="c429b-118">Specifies the group ID.</span></span>
<span data-ttu-id="c429b-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c429b-119">This parameter is required.</span></span>

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

### <span data-ttu-id="c429b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c429b-120">-PassThru</span></span>
<span data-ttu-id="c429b-121">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c429b-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="c429b-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c429b-122">-ProductId</span></span>
<span data-ttu-id="c429b-123">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="c429b-123">Specifies the product ID.</span></span>
<span data-ttu-id="c429b-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c429b-124">This parameter is required.</span></span>

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

### <span data-ttu-id="c429b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c429b-125">CommonParameters</span></span>
<span data-ttu-id="c429b-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c429b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c429b-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c429b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c429b-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c429b-128">INPUTS</span></span>

### <span data-ttu-id="c429b-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c429b-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c429b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c429b-130">System.String</span></span>

### <span data-ttu-id="c429b-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c429b-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c429b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c429b-132">OUTPUTS</span></span>

### <span data-ttu-id="c429b-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c429b-133">System.Boolean</span></span>

## <span data-ttu-id="c429b-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="c429b-134">NOTES</span></span>

## <span data-ttu-id="c429b-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c429b-135">RELATED LINKS</span></span>

[<span data-ttu-id="c429b-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="c429b-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


