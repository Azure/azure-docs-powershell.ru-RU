---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: a92387392c540c75cfa96ecaf4c4acf026ade9f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080126"
---
# <span data-ttu-id="2a132-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="2a132-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="2a132-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a132-102">SYNOPSIS</span></span>
<span data-ttu-id="2a132-103">Добавляет продукт в группу.</span><span class="sxs-lookup"><span data-stu-id="2a132-103">Adds a product to a group.</span></span>

## <span data-ttu-id="2a132-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a132-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a132-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a132-105">DESCRIPTION</span></span>
<span data-ttu-id="2a132-106">Командлет **Add-AzApiManagementProductToGroup** добавляет продукт в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="2a132-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="2a132-107">Другими словами, этот командлет назначает группу для продукта.</span><span class="sxs-lookup"><span data-stu-id="2a132-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="2a132-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a132-108">EXAMPLES</span></span>

### <span data-ttu-id="2a132-109">Пример 1: Добавление продукта в группу</span><span class="sxs-lookup"><span data-stu-id="2a132-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="2a132-110">Эта команда добавляет продукт в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="2a132-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="2a132-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a132-111">PARAMETERS</span></span>

### <span data-ttu-id="2a132-112">-Context</span><span class="sxs-lookup"><span data-stu-id="2a132-112">-Context</span></span>
<span data-ttu-id="2a132-113">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2a132-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="2a132-114">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2a132-114">This parameter is required.</span></span>

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

### <span data-ttu-id="2a132-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a132-115">-DefaultProfile</span></span>
<span data-ttu-id="2a132-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a132-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a132-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="2a132-117">-GroupId</span></span>
<span data-ttu-id="2a132-118">Указывает код группы.</span><span class="sxs-lookup"><span data-stu-id="2a132-118">Specifies the group ID.</span></span>
<span data-ttu-id="2a132-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2a132-119">This parameter is required.</span></span>

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

### <span data-ttu-id="2a132-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a132-120">-PassThru</span></span>
<span data-ttu-id="2a132-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="2a132-121">passthru</span></span>

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

### <span data-ttu-id="2a132-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="2a132-122">-ProductId</span></span>
<span data-ttu-id="2a132-123">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="2a132-123">Specifies the product ID.</span></span>
<span data-ttu-id="2a132-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2a132-124">This parameter is required.</span></span>

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

### <span data-ttu-id="2a132-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a132-125">CommonParameters</span></span>
<span data-ttu-id="2a132-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a132-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a132-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a132-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a132-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a132-128">INPUTS</span></span>

### <span data-ttu-id="2a132-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2a132-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2a132-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2a132-130">System.String</span></span>

### <span data-ttu-id="2a132-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2a132-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2a132-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a132-132">OUTPUTS</span></span>

### <span data-ttu-id="2a132-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a132-133">System.Boolean</span></span>

## <span data-ttu-id="2a132-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a132-134">NOTES</span></span>

## <span data-ttu-id="2a132-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a132-135">RELATED LINKS</span></span>

[<span data-ttu-id="2a132-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="2a132-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


