---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: b4e1a029eca4e7eda48f44d85292639767eaf845
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567197"
---
# <span data-ttu-id="4f2eb-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="4f2eb-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="4f2eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f2eb-102">SYNOPSIS</span></span>
<span data-ttu-id="4f2eb-103">Добавляет продукт в группу.</span><span class="sxs-lookup"><span data-stu-id="4f2eb-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f2eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f2eb-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f2eb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f2eb-105">DESCRIPTION</span></span>
<span data-ttu-id="4f2eb-106">Командлет **Add-AzureRmApiManagementProductToGroup** добавляет продукт в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="4f2eb-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="4f2eb-107">Другими словами, этот командлет назначает группу для продукта.</span><span class="sxs-lookup"><span data-stu-id="4f2eb-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="4f2eb-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f2eb-108">EXAMPLES</span></span>

### <span data-ttu-id="4f2eb-109">Пример 1: Добавление продукта в группу</span><span class="sxs-lookup"><span data-stu-id="4f2eb-109">Example 1: Add a product to a group</span></span>
```
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="4f2eb-110">Эта команда добавляет продукт в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="4f2eb-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="4f2eb-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f2eb-111">PARAMETERS</span></span>

### <span data-ttu-id="4f2eb-112">-Context</span><span class="sxs-lookup"><span data-stu-id="4f2eb-112">-Context</span></span>
<span data-ttu-id="4f2eb-113">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4f2eb-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="4f2eb-114">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="4f2eb-114">This parameter is required.</span></span>

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

### <span data-ttu-id="4f2eb-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="4f2eb-115">-GroupId</span></span>
<span data-ttu-id="4f2eb-116">Указывает код группы.</span><span class="sxs-lookup"><span data-stu-id="4f2eb-116">Specifies the group ID.</span></span>
<span data-ttu-id="4f2eb-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="4f2eb-117">This parameter is required.</span></span>

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

### <span data-ttu-id="4f2eb-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f2eb-118">-PassThru</span></span>
<span data-ttu-id="4f2eb-119">PassThru</span><span class="sxs-lookup"><span data-stu-id="4f2eb-119">passthru</span></span>

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

### <span data-ttu-id="4f2eb-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="4f2eb-120">-ProductId</span></span>
<span data-ttu-id="4f2eb-121">Указывает код продукта.</span><span class="sxs-lookup"><span data-stu-id="4f2eb-121">Specifies the product ID.</span></span>
<span data-ttu-id="4f2eb-122">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="4f2eb-122">This parameter is required.</span></span>

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

### <span data-ttu-id="4f2eb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f2eb-123">-DefaultProfile</span></span>
<span data-ttu-id="4f2eb-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f2eb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f2eb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f2eb-125">CommonParameters</span></span>
<span data-ttu-id="4f2eb-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f2eb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f2eb-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f2eb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f2eb-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f2eb-128">INPUTS</span></span>

## <span data-ttu-id="4f2eb-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f2eb-129">OUTPUTS</span></span>

### <span data-ttu-id="4f2eb-130">Значением</span><span class="sxs-lookup"><span data-stu-id="4f2eb-130">Boolean</span></span>

## <span data-ttu-id="4f2eb-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f2eb-131">NOTES</span></span>

## <span data-ttu-id="4f2eb-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f2eb-132">RELATED LINKS</span></span>

[<span data-ttu-id="4f2eb-133">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="4f2eb-133">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


