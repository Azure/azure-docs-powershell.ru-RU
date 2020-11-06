---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 31ab005953ea405dc8aac093f973a6e842974814
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567323"
---
# <span data-ttu-id="eb003-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="eb003-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="eb003-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb003-102">SYNOPSIS</span></span>
<span data-ttu-id="eb003-103">Удаление существующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="eb003-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb003-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb003-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb003-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb003-105">DESCRIPTION</span></span>
<span data-ttu-id="eb003-106">Командлет **Remove-AzureRmApiManagementUser** удаляет существующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="eb003-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="eb003-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb003-107">EXAMPLES</span></span>

### <span data-ttu-id="eb003-108">Пример 1: Удаление пользователя</span><span class="sxs-lookup"><span data-stu-id="eb003-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="eb003-109">Эта команда удаляет существующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="eb003-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="eb003-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb003-110">PARAMETERS</span></span>

### <span data-ttu-id="eb003-111">-Context</span><span class="sxs-lookup"><span data-stu-id="eb003-111">-Context</span></span>
<span data-ttu-id="eb003-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="eb003-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="eb003-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="eb003-113">This parameter is required.</span></span>

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

### <span data-ttu-id="eb003-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb003-114">-DefaultProfile</span></span>
<span data-ttu-id="eb003-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb003-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb003-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="eb003-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="eb003-117">Указывает, нужно ли удалять подписку на продукт.</span><span class="sxs-lookup"><span data-stu-id="eb003-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="eb003-118">Если этот параметр не указан, а подписка существует, этот командлет создает исключение.</span><span class="sxs-lookup"><span data-stu-id="eb003-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="eb003-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="eb003-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="eb003-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb003-120">-PassThru</span></span>
<span data-ttu-id="eb003-121">Указывает на то, что этот командлет возвращает значение $Ture, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="eb003-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="eb003-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="eb003-122">-UserId</span></span>
<span data-ttu-id="eb003-123">Указывает ИД пользователя, которого нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="eb003-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="eb003-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb003-124">-Confirm</span></span>
<span data-ttu-id="eb003-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eb003-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb003-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb003-126">-WhatIf</span></span>
<span data-ttu-id="eb003-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eb003-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb003-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eb003-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb003-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb003-129">CommonParameters</span></span>
<span data-ttu-id="eb003-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb003-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb003-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb003-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb003-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb003-132">INPUTS</span></span>

### <span data-ttu-id="eb003-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="eb003-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="eb003-134">System. String</span><span class="sxs-lookup"><span data-stu-id="eb003-134">System.String</span></span>

### <span data-ttu-id="eb003-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eb003-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eb003-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb003-136">OUTPUTS</span></span>

### <span data-ttu-id="eb003-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb003-137">System.Boolean</span></span>

## <span data-ttu-id="eb003-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb003-138">NOTES</span></span>

## <span data-ttu-id="eb003-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb003-139">RELATED LINKS</span></span>

[<span data-ttu-id="eb003-140">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="eb003-140">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="eb003-141">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="eb003-141">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="eb003-142">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="eb003-142">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


