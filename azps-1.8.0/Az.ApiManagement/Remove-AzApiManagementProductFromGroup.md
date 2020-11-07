---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: 154b8ee52f1f0456845d0648c64c4c3e3484ecd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901637"
---
# <span data-ttu-id="1790a-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="1790a-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="1790a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1790a-102">SYNOPSIS</span></span>
<span data-ttu-id="1790a-103">Удаление продукта из группы.</span><span class="sxs-lookup"><span data-stu-id="1790a-103">Removes a product from a group.</span></span>

## <span data-ttu-id="1790a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1790a-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1790a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1790a-105">DESCRIPTION</span></span>
<span data-ttu-id="1790a-106">Командлет **Remove-AzApiManagementProductFromGroup** удаляет продукт из существующей группы.</span><span class="sxs-lookup"><span data-stu-id="1790a-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="1790a-107">Другими словами, этот командлет удаляет назначение групп из продукта.</span><span class="sxs-lookup"><span data-stu-id="1790a-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="1790a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1790a-108">EXAMPLES</span></span>

### <span data-ttu-id="1790a-109">Пример 1: удаление продукта из группы</span><span class="sxs-lookup"><span data-stu-id="1790a-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="1790a-110">Эта команда удаляет продукт из существующей группы.</span><span class="sxs-lookup"><span data-stu-id="1790a-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="1790a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1790a-111">PARAMETERS</span></span>

### <span data-ttu-id="1790a-112">-Context</span><span class="sxs-lookup"><span data-stu-id="1790a-112">-Context</span></span>
<span data-ttu-id="1790a-113">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1790a-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="1790a-114">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1790a-114">This parameter is required.</span></span>

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

### <span data-ttu-id="1790a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1790a-115">-DefaultProfile</span></span>
<span data-ttu-id="1790a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1790a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1790a-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="1790a-117">-GroupId</span></span>
<span data-ttu-id="1790a-118">Указывает код группы.</span><span class="sxs-lookup"><span data-stu-id="1790a-118">Specifies the group ID.</span></span>
<span data-ttu-id="1790a-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1790a-119">This parameter is required.</span></span>

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

### <span data-ttu-id="1790a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1790a-120">-PassThru</span></span>
<span data-ttu-id="1790a-121">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1790a-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="1790a-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="1790a-122">-ProductId</span></span>
<span data-ttu-id="1790a-123">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="1790a-123">Specifies the product ID.</span></span>
<span data-ttu-id="1790a-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1790a-124">This parameter is required.</span></span>

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

### <span data-ttu-id="1790a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1790a-125">CommonParameters</span></span>
<span data-ttu-id="1790a-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1790a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1790a-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1790a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1790a-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1790a-128">INPUTS</span></span>

### <span data-ttu-id="1790a-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1790a-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1790a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1790a-130">System.String</span></span>

### <span data-ttu-id="1790a-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1790a-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1790a-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1790a-132">OUTPUTS</span></span>

### <span data-ttu-id="1790a-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1790a-133">System.Boolean</span></span>

## <span data-ttu-id="1790a-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="1790a-134">NOTES</span></span>

## <span data-ttu-id="1790a-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1790a-135">RELATED LINKS</span></span>

[<span data-ttu-id="1790a-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="1790a-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


