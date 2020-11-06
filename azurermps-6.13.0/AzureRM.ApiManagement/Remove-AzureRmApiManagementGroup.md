---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
ms.openlocfilehash: d297c4f8bb9999d60ec694c73aa723dd4afec58f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556932"
---
# <span data-ttu-id="caea1-101">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="caea1-101">Remove-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="caea1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="caea1-102">SYNOPSIS</span></span>
<span data-ttu-id="caea1-103">Удаляет существующую группу управления API.</span><span class="sxs-lookup"><span data-stu-id="caea1-103">Removes an existing API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caea1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="caea1-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caea1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="caea1-105">DESCRIPTION</span></span>
<span data-ttu-id="caea1-106">Командлет **Remove-AzureRmApiManagementGroup** удаляет существующую группу управления API.</span><span class="sxs-lookup"><span data-stu-id="caea1-106">The **Remove-AzureRmApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="caea1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="caea1-107">EXAMPLES</span></span>

### <span data-ttu-id="caea1-108">Пример 1: удаление существующей группы управления</span><span class="sxs-lookup"><span data-stu-id="caea1-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="caea1-109">Эта команда удаляет существующую группу управления с именем Group0001 и не запрашивает подтверждение у пользователя.</span><span class="sxs-lookup"><span data-stu-id="caea1-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="caea1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="caea1-110">PARAMETERS</span></span>

### <span data-ttu-id="caea1-111">-Context</span><span class="sxs-lookup"><span data-stu-id="caea1-111">-Context</span></span>
<span data-ttu-id="caea1-112">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="caea1-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="caea1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caea1-113">-DefaultProfile</span></span>
<span data-ttu-id="caea1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="caea1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="caea1-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="caea1-115">-GroupId</span></span>
<span data-ttu-id="caea1-116">Указывает идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="caea1-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="caea1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="caea1-117">-PassThru</span></span>
<span data-ttu-id="caea1-118">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="caea1-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="caea1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="caea1-119">-Confirm</span></span>
<span data-ttu-id="caea1-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="caea1-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caea1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caea1-121">-WhatIf</span></span>
<span data-ttu-id="caea1-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="caea1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caea1-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="caea1-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caea1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caea1-124">CommonParameters</span></span>
<span data-ttu-id="caea1-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="caea1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caea1-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caea1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caea1-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="caea1-127">INPUTS</span></span>

### <span data-ttu-id="caea1-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="caea1-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="caea1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="caea1-129">System.String</span></span>

### <span data-ttu-id="caea1-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="caea1-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="caea1-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="caea1-131">OUTPUTS</span></span>

### <span data-ttu-id="caea1-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="caea1-132">System.Boolean</span></span>

## <span data-ttu-id="caea1-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="caea1-133">NOTES</span></span>

## <span data-ttu-id="caea1-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="caea1-134">RELATED LINKS</span></span>

[<span data-ttu-id="caea1-135">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="caea1-135">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="caea1-136">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="caea1-136">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="caea1-137">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="caea1-137">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


