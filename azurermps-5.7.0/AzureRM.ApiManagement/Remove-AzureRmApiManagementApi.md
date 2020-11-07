---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: 4bcda06e1c00e338feb80584fb6e2b51a63b051d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734740"
---
# <span data-ttu-id="2f069-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f069-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="2f069-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f069-102">SYNOPSIS</span></span>
<span data-ttu-id="2f069-103">Удаляет API.</span><span class="sxs-lookup"><span data-stu-id="2f069-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f069-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f069-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f069-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f069-105">DESCRIPTION</span></span>
<span data-ttu-id="2f069-106">Командлет **Remove-AzureRmApiManagementApi** УДАЛЯЕТ существующий API.</span><span class="sxs-lookup"><span data-stu-id="2f069-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="2f069-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f069-107">EXAMPLES</span></span>

### <span data-ttu-id="2f069-108">Пример 1: удаление API</span><span class="sxs-lookup"><span data-stu-id="2f069-108">Example 1: Remove an API</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="2f069-109">Эта команда удаляет API с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="2f069-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="2f069-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f069-110">PARAMETERS</span></span>

### <span data-ttu-id="2f069-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2f069-111">-ApiId</span></span>
<span data-ttu-id="2f069-112">Указывает идентификатор API Remove.</span><span class="sxs-lookup"><span data-stu-id="2f069-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="2f069-113">-Context</span><span class="sxs-lookup"><span data-stu-id="2f069-113">-Context</span></span>
<span data-ttu-id="2f069-114">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2f069-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2f069-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f069-115">-DefaultProfile</span></span>
<span data-ttu-id="2f069-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f069-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="2f069-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f069-117">-PassThru</span></span>
<span data-ttu-id="2f069-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="2f069-118">passthru</span></span>

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

### <span data-ttu-id="2f069-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f069-119">-Confirm</span></span>
<span data-ttu-id="2f069-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f069-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f069-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f069-121">-WhatIf</span></span>
<span data-ttu-id="2f069-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f069-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f069-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f069-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f069-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f069-124">CommonParameters</span></span>
<span data-ttu-id="2f069-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f069-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f069-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f069-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f069-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f069-127">INPUTS</span></span>

### <span data-ttu-id="2f069-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="2f069-128">None</span></span>
<span data-ttu-id="2f069-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2f069-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f069-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f069-130">OUTPUTS</span></span>

### <span data-ttu-id="2f069-131">Значением</span><span class="sxs-lookup"><span data-stu-id="2f069-131">Boolean</span></span>

## <span data-ttu-id="2f069-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f069-132">NOTES</span></span>

## <span data-ttu-id="2f069-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f069-133">RELATED LINKS</span></span>

[<span data-ttu-id="2f069-134">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f069-134">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="2f069-135">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f069-135">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="2f069-136">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f069-136">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="2f069-137">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f069-137">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="2f069-138">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f069-138">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


