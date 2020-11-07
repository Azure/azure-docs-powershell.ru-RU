---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: f7c1db6b4ce7c9df63506cdba8b1a206c22ee03e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735008"
---
# <span data-ttu-id="c9d50-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="c9d50-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="c9d50-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9d50-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d50-103">Добавляет продукт в группу.</span><span class="sxs-lookup"><span data-stu-id="c9d50-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9d50-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9d50-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9d50-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9d50-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d50-106">Командлет **Add-AzureRmApiManagementProductToGroup** добавляет продукт в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="c9d50-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="c9d50-107">Другими словами, этот командлет назначает группу для продукта.</span><span class="sxs-lookup"><span data-stu-id="c9d50-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="c9d50-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9d50-108">EXAMPLES</span></span>

### <span data-ttu-id="c9d50-109">Пример 1: Добавление продукта в группу</span><span class="sxs-lookup"><span data-stu-id="c9d50-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="c9d50-110">Эта команда добавляет продукт в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="c9d50-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="c9d50-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9d50-111">PARAMETERS</span></span>

### <span data-ttu-id="c9d50-112">-Context</span><span class="sxs-lookup"><span data-stu-id="c9d50-112">-Context</span></span>
<span data-ttu-id="c9d50-113">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c9d50-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="c9d50-114">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c9d50-114">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d50-115">-DefaultProfile</span></span>
<span data-ttu-id="c9d50-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9d50-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d50-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="c9d50-117">-GroupId</span></span>
<span data-ttu-id="c9d50-118">Указывает код группы.</span><span class="sxs-lookup"><span data-stu-id="c9d50-118">Specifies the group ID.</span></span>
<span data-ttu-id="c9d50-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c9d50-119">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d50-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9d50-120">-PassThru</span></span>
<span data-ttu-id="c9d50-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="c9d50-121">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d50-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c9d50-122">-ProductId</span></span>
<span data-ttu-id="c9d50-123">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="c9d50-123">Specifies the product ID.</span></span>
<span data-ttu-id="c9d50-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c9d50-124">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d50-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d50-125">CommonParameters</span></span>
<span data-ttu-id="c9d50-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9d50-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d50-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d50-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d50-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9d50-128">INPUTS</span></span>

### <span data-ttu-id="c9d50-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="c9d50-129">None</span></span>
<span data-ttu-id="c9d50-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c9d50-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9d50-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9d50-131">OUTPUTS</span></span>

### <span data-ttu-id="c9d50-132">Значением</span><span class="sxs-lookup"><span data-stu-id="c9d50-132">Boolean</span></span>

## <span data-ttu-id="c9d50-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9d50-133">NOTES</span></span>

## <span data-ttu-id="c9d50-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9d50-134">RELATED LINKS</span></span>

[<span data-ttu-id="c9d50-135">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="c9d50-135">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


