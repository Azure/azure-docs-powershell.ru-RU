---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 6be4c714627d77b0e3c56b8dd9766c550deebd7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557980"
---
# <span data-ttu-id="6b87a-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="6b87a-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="6b87a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b87a-102">SYNOPSIS</span></span>
<span data-ttu-id="6b87a-103">Удаление существующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b87a-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b87a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b87a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b87a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b87a-105">DESCRIPTION</span></span>
<span data-ttu-id="6b87a-106">Командлет **Remove-AzureRmApiManagementUser** удаляет существующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b87a-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="6b87a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b87a-107">EXAMPLES</span></span>

### <span data-ttu-id="6b87a-108">Пример 1: Удаление пользователя</span><span class="sxs-lookup"><span data-stu-id="6b87a-108">Example 1: Delete a user</span></span>
```
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="6b87a-109">Эта команда удаляет существующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b87a-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="6b87a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b87a-110">PARAMETERS</span></span>

### <span data-ttu-id="6b87a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6b87a-111">-Context</span></span>
<span data-ttu-id="6b87a-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6b87a-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="6b87a-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6b87a-113">This parameter is required.</span></span>

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

### <span data-ttu-id="6b87a-114">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="6b87a-114">-DeleteSubscriptions</span></span>
<span data-ttu-id="6b87a-115">Указывает, нужно ли удалять подписку на продукт.</span><span class="sxs-lookup"><span data-stu-id="6b87a-115">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="6b87a-116">Если этот параметр не указан, а подписка существует, этот командлет создает исключение.</span><span class="sxs-lookup"><span data-stu-id="6b87a-116">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="6b87a-117">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6b87a-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="6b87a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b87a-118">-PassThru</span></span>
<span data-ttu-id="6b87a-119">Указывает на то, что этот командлет возвращает значение $Ture, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6b87a-119">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="6b87a-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="6b87a-120">-UserId</span></span>
<span data-ttu-id="6b87a-121">Указывает ИД пользователя, которого нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6b87a-121">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="6b87a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b87a-122">-Confirm</span></span>
<span data-ttu-id="6b87a-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6b87a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b87a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b87a-124">-WhatIf</span></span>
<span data-ttu-id="6b87a-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6b87a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b87a-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6b87a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b87a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b87a-127">-DefaultProfile</span></span>
<span data-ttu-id="6b87a-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b87a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b87a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b87a-129">CommonParameters</span></span>
<span data-ttu-id="6b87a-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b87a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b87a-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b87a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b87a-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b87a-132">INPUTS</span></span>

## <span data-ttu-id="6b87a-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b87a-133">OUTPUTS</span></span>

### <span data-ttu-id="6b87a-134">Значением</span><span class="sxs-lookup"><span data-stu-id="6b87a-134">Boolean</span></span>

## <span data-ttu-id="6b87a-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b87a-135">NOTES</span></span>

## <span data-ttu-id="6b87a-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b87a-136">RELATED LINKS</span></span>

[<span data-ttu-id="6b87a-137">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="6b87a-137">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="6b87a-138">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="6b87a-138">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="6b87a-139">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="6b87a-139">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


