---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: 4c90b51a316db63bad2e5481e1b6390849d83292
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246151"
---
# <span data-ttu-id="03eab-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="03eab-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="03eab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03eab-102">SYNOPSIS</span></span>
<span data-ttu-id="03eab-103">Удаление существующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="03eab-103">Deletes an existing user.</span></span>

## <span data-ttu-id="03eab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03eab-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03eab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03eab-105">DESCRIPTION</span></span>
<span data-ttu-id="03eab-106">Командлет **Remove-AzApiManagementUser** удаляет существующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="03eab-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="03eab-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03eab-107">EXAMPLES</span></span>

### <span data-ttu-id="03eab-108">Пример 1: Удаление пользователя</span><span class="sxs-lookup"><span data-stu-id="03eab-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="03eab-109">Эта команда удаляет существующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="03eab-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="03eab-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03eab-110">PARAMETERS</span></span>

### <span data-ttu-id="03eab-111">-Context</span><span class="sxs-lookup"><span data-stu-id="03eab-111">-Context</span></span>
<span data-ttu-id="03eab-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="03eab-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="03eab-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="03eab-113">This parameter is required.</span></span>

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

### <span data-ttu-id="03eab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03eab-114">-DefaultProfile</span></span>
<span data-ttu-id="03eab-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="03eab-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03eab-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="03eab-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="03eab-117">Указывает, нужно ли удалять подписку на продукт.</span><span class="sxs-lookup"><span data-stu-id="03eab-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="03eab-118">Если этот параметр не указан, а подписка существует, этот командлет создает исключение.</span><span class="sxs-lookup"><span data-stu-id="03eab-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="03eab-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="03eab-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="03eab-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03eab-120">-PassThru</span></span>
<span data-ttu-id="03eab-121">Указывает на то, что этот командлет возвращает значение $Ture, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="03eab-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="03eab-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="03eab-122">-UserId</span></span>
<span data-ttu-id="03eab-123">Указывает ИД пользователя, которого нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="03eab-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="03eab-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03eab-124">-Confirm</span></span>
<span data-ttu-id="03eab-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="03eab-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03eab-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03eab-126">-WhatIf</span></span>
<span data-ttu-id="03eab-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="03eab-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03eab-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="03eab-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03eab-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03eab-129">CommonParameters</span></span>
<span data-ttu-id="03eab-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03eab-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03eab-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03eab-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03eab-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03eab-132">INPUTS</span></span>

### <span data-ttu-id="03eab-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="03eab-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="03eab-134">System. String</span><span class="sxs-lookup"><span data-stu-id="03eab-134">System.String</span></span>

### <span data-ttu-id="03eab-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="03eab-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="03eab-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03eab-136">OUTPUTS</span></span>

### <span data-ttu-id="03eab-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03eab-137">System.Boolean</span></span>

## <span data-ttu-id="03eab-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="03eab-138">NOTES</span></span>

## <span data-ttu-id="03eab-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03eab-139">RELATED LINKS</span></span>

[<span data-ttu-id="03eab-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="03eab-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="03eab-141">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="03eab-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="03eab-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="03eab-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


