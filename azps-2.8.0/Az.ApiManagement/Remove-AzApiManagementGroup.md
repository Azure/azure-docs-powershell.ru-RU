---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 561bec75ecfe59c65b2b8ea6ac71364573aa2bcd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727989"
---
# <span data-ttu-id="35c8d-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="35c8d-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="35c8d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="35c8d-103">Удаляет существующую группу управления API.</span><span class="sxs-lookup"><span data-stu-id="35c8d-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="35c8d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35c8d-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35c8d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35c8d-105">DESCRIPTION</span></span>
<span data-ttu-id="35c8d-106">Командлет **Remove-AzApiManagementGroup** удаляет существующую группу управления API.</span><span class="sxs-lookup"><span data-stu-id="35c8d-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="35c8d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35c8d-107">EXAMPLES</span></span>

### <span data-ttu-id="35c8d-108">Пример 1: удаление существующей группы управления</span><span class="sxs-lookup"><span data-stu-id="35c8d-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="35c8d-109">Эта команда удаляет существующую группу управления с именем Group0001 и не запрашивает подтверждение у пользователя.</span><span class="sxs-lookup"><span data-stu-id="35c8d-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="35c8d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35c8d-110">PARAMETERS</span></span>

### <span data-ttu-id="35c8d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="35c8d-111">-Context</span></span>
<span data-ttu-id="35c8d-112">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="35c8d-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="35c8d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35c8d-113">-DefaultProfile</span></span>
<span data-ttu-id="35c8d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35c8d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35c8d-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="35c8d-115">-GroupId</span></span>
<span data-ttu-id="35c8d-116">Указывает идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="35c8d-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="35c8d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35c8d-117">-PassThru</span></span>
<span data-ttu-id="35c8d-118">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="35c8d-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="35c8d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35c8d-119">-Confirm</span></span>
<span data-ttu-id="35c8d-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35c8d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35c8d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35c8d-121">-WhatIf</span></span>
<span data-ttu-id="35c8d-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="35c8d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35c8d-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="35c8d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35c8d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c8d-124">CommonParameters</span></span>
<span data-ttu-id="35c8d-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35c8d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c8d-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35c8d-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c8d-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35c8d-127">INPUTS</span></span>

### <span data-ttu-id="35c8d-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="35c8d-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="35c8d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="35c8d-129">System.String</span></span>

### <span data-ttu-id="35c8d-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="35c8d-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="35c8d-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35c8d-131">OUTPUTS</span></span>

### <span data-ttu-id="35c8d-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35c8d-132">System.Boolean</span></span>

## <span data-ttu-id="35c8d-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="35c8d-133">NOTES</span></span>

## <span data-ttu-id="35c8d-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35c8d-134">RELATED LINKS</span></span>

[<span data-ttu-id="35c8d-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="35c8d-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="35c8d-136">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="35c8d-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="35c8d-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="35c8d-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


