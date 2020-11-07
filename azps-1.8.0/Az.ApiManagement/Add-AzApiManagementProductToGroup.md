---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: 3345b48b7956e9a2e8c82d28dd87ec254bf85544
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720180"
---
# <span data-ttu-id="dc439-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="dc439-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="dc439-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc439-102">SYNOPSIS</span></span>
<span data-ttu-id="dc439-103">Добавляет продукт в группу.</span><span class="sxs-lookup"><span data-stu-id="dc439-103">Adds a product to a group.</span></span>

## <span data-ttu-id="dc439-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc439-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc439-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc439-105">DESCRIPTION</span></span>
<span data-ttu-id="dc439-106">Командлет **Add-AzApiManagementProductToGroup** добавляет продукт в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="dc439-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="dc439-107">Другими словами, этот командлет назначает группу для продукта.</span><span class="sxs-lookup"><span data-stu-id="dc439-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="dc439-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc439-108">EXAMPLES</span></span>

### <span data-ttu-id="dc439-109">Пример 1: Добавление продукта в группу</span><span class="sxs-lookup"><span data-stu-id="dc439-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="dc439-110">Эта команда добавляет продукт в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="dc439-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="dc439-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc439-111">PARAMETERS</span></span>

### <span data-ttu-id="dc439-112">-Context</span><span class="sxs-lookup"><span data-stu-id="dc439-112">-Context</span></span>
<span data-ttu-id="dc439-113">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="dc439-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="dc439-114">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="dc439-114">This parameter is required.</span></span>

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

### <span data-ttu-id="dc439-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc439-115">-DefaultProfile</span></span>
<span data-ttu-id="dc439-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc439-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc439-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="dc439-117">-GroupId</span></span>
<span data-ttu-id="dc439-118">Указывает код группы.</span><span class="sxs-lookup"><span data-stu-id="dc439-118">Specifies the group ID.</span></span>
<span data-ttu-id="dc439-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="dc439-119">This parameter is required.</span></span>

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

### <span data-ttu-id="dc439-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc439-120">-PassThru</span></span>
<span data-ttu-id="dc439-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="dc439-121">passthru</span></span>

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

### <span data-ttu-id="dc439-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="dc439-122">-ProductId</span></span>
<span data-ttu-id="dc439-123">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="dc439-123">Specifies the product ID.</span></span>
<span data-ttu-id="dc439-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="dc439-124">This parameter is required.</span></span>

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

### <span data-ttu-id="dc439-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc439-125">CommonParameters</span></span>
<span data-ttu-id="dc439-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc439-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc439-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc439-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc439-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc439-128">INPUTS</span></span>

### <span data-ttu-id="dc439-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dc439-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dc439-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dc439-130">System.String</span></span>

### <span data-ttu-id="dc439-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dc439-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dc439-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc439-132">OUTPUTS</span></span>

### <span data-ttu-id="dc439-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc439-133">System.Boolean</span></span>

## <span data-ttu-id="dc439-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc439-134">NOTES</span></span>

## <span data-ttu-id="dc439-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc439-135">RELATED LINKS</span></span>

[<span data-ttu-id="dc439-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="dc439-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


