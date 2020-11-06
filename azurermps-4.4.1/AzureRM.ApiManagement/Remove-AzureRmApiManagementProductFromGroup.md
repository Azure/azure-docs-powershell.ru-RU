---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
ms.openlocfilehash: a6ef7e141863b6dfd98185df0f8e3cfbd85ae40b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558000"
---
# <span data-ttu-id="12110-101">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="12110-101">Remove-AzureRmApiManagementProductFromGroup</span></span>

## <span data-ttu-id="12110-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12110-102">SYNOPSIS</span></span>
<span data-ttu-id="12110-103">Удаление продукта из группы.</span><span class="sxs-lookup"><span data-stu-id="12110-103">Removes a product from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12110-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12110-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String>
 -ProductId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12110-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12110-105">DESCRIPTION</span></span>
<span data-ttu-id="12110-106">Командлет **Remove-AzureRmApiManagementProductFromGroup** удаляет продукт из существующей группы.</span><span class="sxs-lookup"><span data-stu-id="12110-106">The **Remove-AzureRmApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="12110-107">Другими словами, этот командлет удаляет назначение групп из продукта.</span><span class="sxs-lookup"><span data-stu-id="12110-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="12110-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12110-108">EXAMPLES</span></span>

### <span data-ttu-id="12110-109">Пример 1: удаление продукта из группы</span><span class="sxs-lookup"><span data-stu-id="12110-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>Remove-AzureRmApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="12110-110">Эта команда удаляет продукт из существующей группы.</span><span class="sxs-lookup"><span data-stu-id="12110-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="12110-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12110-111">PARAMETERS</span></span>

### <span data-ttu-id="12110-112">-Context</span><span class="sxs-lookup"><span data-stu-id="12110-112">-Context</span></span>
<span data-ttu-id="12110-113">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="12110-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="12110-114">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="12110-114">This parameter is required.</span></span>

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

### <span data-ttu-id="12110-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="12110-115">-GroupId</span></span>
<span data-ttu-id="12110-116">Указывает код группы.</span><span class="sxs-lookup"><span data-stu-id="12110-116">Specifies the group ID.</span></span>
<span data-ttu-id="12110-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="12110-117">This parameter is required.</span></span>

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

### <span data-ttu-id="12110-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12110-118">-PassThru</span></span>
<span data-ttu-id="12110-119">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="12110-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="12110-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="12110-120">-ProductId</span></span>
<span data-ttu-id="12110-121">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="12110-121">Specifies the product ID.</span></span>
<span data-ttu-id="12110-122">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="12110-122">This parameter is required.</span></span>

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

### <span data-ttu-id="12110-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12110-123">-DefaultProfile</span></span>
<span data-ttu-id="12110-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12110-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12110-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12110-125">CommonParameters</span></span>
<span data-ttu-id="12110-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12110-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12110-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12110-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12110-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12110-128">INPUTS</span></span>

## <span data-ttu-id="12110-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12110-129">OUTPUTS</span></span>

### <span data-ttu-id="12110-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12110-130">System.Boolean</span></span>

## <span data-ttu-id="12110-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="12110-131">NOTES</span></span>

## <span data-ttu-id="12110-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12110-132">RELATED LINKS</span></span>

[<span data-ttu-id="12110-133">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="12110-133">Add-AzureRmApiManagementProductToGroup</span></span>](./Add-AzureRmApiManagementProductToGroup.md)


