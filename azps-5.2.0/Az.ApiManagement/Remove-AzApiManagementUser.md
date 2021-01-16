---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: 4c90b51a316db63bad2e5481e1b6390849d83292
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397652"
---
# <span data-ttu-id="052ac-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="052ac-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="052ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="052ac-102">SYNOPSIS</span></span>
<span data-ttu-id="052ac-103">Удаляет существующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="052ac-103">Deletes an existing user.</span></span>

## <span data-ttu-id="052ac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="052ac-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="052ac-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="052ac-105">DESCRIPTION</span></span>
<span data-ttu-id="052ac-106">С **его учетной** записью будет удален существующий пользователь.</span><span class="sxs-lookup"><span data-stu-id="052ac-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="052ac-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="052ac-107">EXAMPLES</span></span>

### <span data-ttu-id="052ac-108">Пример 1. Удаление пользователя</span><span class="sxs-lookup"><span data-stu-id="052ac-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="052ac-109">Эта команда удаляет существующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="052ac-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="052ac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="052ac-110">PARAMETERS</span></span>

### <span data-ttu-id="052ac-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="052ac-111">-Context</span></span>
<span data-ttu-id="052ac-112">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="052ac-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="052ac-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="052ac-113">This parameter is required.</span></span>

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

### <span data-ttu-id="052ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="052ac-114">-DefaultProfile</span></span>
<span data-ttu-id="052ac-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="052ac-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="052ac-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="052ac-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="052ac-117">Указывает, нужно ли удалять подписки на продукт.</span><span class="sxs-lookup"><span data-stu-id="052ac-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="052ac-118">Если этот параметр не указан и подписка существует, этот cmdlet выдает исключение.</span><span class="sxs-lookup"><span data-stu-id="052ac-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="052ac-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="052ac-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="052ac-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="052ac-120">-PassThru</span></span>
<span data-ttu-id="052ac-121">Указывает на то, что этот $Ture возвращает значение $Ture, если он успешно, или значение $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="052ac-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="052ac-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="052ac-122">-UserId</span></span>
<span data-ttu-id="052ac-123">Определяет ИД пользователя, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="052ac-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="052ac-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="052ac-124">-Confirm</span></span>
<span data-ttu-id="052ac-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="052ac-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="052ac-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="052ac-126">-WhatIf</span></span>
<span data-ttu-id="052ac-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="052ac-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="052ac-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="052ac-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="052ac-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="052ac-129">CommonParameters</span></span>
<span data-ttu-id="052ac-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="052ac-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="052ac-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="052ac-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="052ac-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="052ac-132">INPUTS</span></span>

### <span data-ttu-id="052ac-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="052ac-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="052ac-134">System.String</span><span class="sxs-lookup"><span data-stu-id="052ac-134">System.String</span></span>

### <span data-ttu-id="052ac-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="052ac-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="052ac-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="052ac-136">OUTPUTS</span></span>

### <span data-ttu-id="052ac-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="052ac-137">System.Boolean</span></span>

## <span data-ttu-id="052ac-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="052ac-138">NOTES</span></span>

## <span data-ttu-id="052ac-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="052ac-139">RELATED LINKS</span></span>

[<span data-ttu-id="052ac-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="052ac-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="052ac-141">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="052ac-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="052ac-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="052ac-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


