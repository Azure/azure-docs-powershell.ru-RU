---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
ms.openlocfilehash: a5919959f038b94a27f373124377466926494337
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568269"
---
# <span data-ttu-id="40e33-101">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="40e33-101">Remove-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="40e33-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40e33-102">SYNOPSIS</span></span>
<span data-ttu-id="40e33-103">Удаляет существующую группу управления API.</span><span class="sxs-lookup"><span data-stu-id="40e33-103">Removes an existing API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40e33-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40e33-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40e33-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40e33-105">DESCRIPTION</span></span>
<span data-ttu-id="40e33-106">Командлет **Remove-AzureRmApiManagementGroup** удаляет существующую группу управления API.</span><span class="sxs-lookup"><span data-stu-id="40e33-106">The **Remove-AzureRmApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="40e33-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40e33-107">EXAMPLES</span></span>

### <span data-ttu-id="40e33-108">Пример 1: удаление существующей группы управления</span><span class="sxs-lookup"><span data-stu-id="40e33-108">Example 1: Remove an existing management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="40e33-109">Эта команда удаляет существующую группу управления с именем Group0001 и не запрашивает подтверждение у пользователя.</span><span class="sxs-lookup"><span data-stu-id="40e33-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="40e33-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40e33-110">PARAMETERS</span></span>

### <span data-ttu-id="40e33-111">-Context</span><span class="sxs-lookup"><span data-stu-id="40e33-111">-Context</span></span>
<span data-ttu-id="40e33-112">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="40e33-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="40e33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e33-113">-DefaultProfile</span></span>
<span data-ttu-id="40e33-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40e33-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="40e33-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="40e33-115">-GroupId</span></span>
<span data-ttu-id="40e33-116">Указывает идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="40e33-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="40e33-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40e33-117">-PassThru</span></span>
<span data-ttu-id="40e33-118">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="40e33-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="40e33-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40e33-119">-Confirm</span></span>
<span data-ttu-id="40e33-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40e33-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40e33-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40e33-121">-WhatIf</span></span>
<span data-ttu-id="40e33-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="40e33-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40e33-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="40e33-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40e33-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e33-124">CommonParameters</span></span>
<span data-ttu-id="40e33-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40e33-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e33-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40e33-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e33-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40e33-127">INPUTS</span></span>

### <span data-ttu-id="40e33-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="40e33-128">None</span></span>
<span data-ttu-id="40e33-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="40e33-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40e33-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40e33-130">OUTPUTS</span></span>

### <span data-ttu-id="40e33-131">Значением</span><span class="sxs-lookup"><span data-stu-id="40e33-131">Boolean</span></span>

## <span data-ttu-id="40e33-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="40e33-132">NOTES</span></span>

## <span data-ttu-id="40e33-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40e33-133">RELATED LINKS</span></span>

[<span data-ttu-id="40e33-134">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="40e33-134">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="40e33-135">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="40e33-135">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="40e33-136">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="40e33-136">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


