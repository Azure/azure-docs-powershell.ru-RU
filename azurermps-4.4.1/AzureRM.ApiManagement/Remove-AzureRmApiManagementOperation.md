---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: 685da9955f272066ec39890ea0f3a063d3b2f9b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559979"
---
# <span data-ttu-id="8a9aa-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8a9aa-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="8a9aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a9aa-102">SYNOPSIS</span></span>
<span data-ttu-id="8a9aa-103">Удаляет существующую операцию.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a9aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a9aa-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a9aa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a9aa-105">DESCRIPTION</span></span>
<span data-ttu-id="8a9aa-106">Командлет **Remove-AzureRmApiManagementOperation** удаляет существующую операцию.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="8a9aa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a9aa-107">EXAMPLES</span></span>

### <span data-ttu-id="8a9aa-108">Пример 1: удаление существующей операции API</span><span class="sxs-lookup"><span data-stu-id="8a9aa-108">Example 1: Remove an existing API Operation</span></span>
```
PS C:\>Remove-AzureRmApiManagementOperation -Context $APImContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="8a9aa-109">Эта команда удаляет существующую операцию API.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="8a9aa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a9aa-110">PARAMETERS</span></span>

### <span data-ttu-id="8a9aa-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8a9aa-111">-ApiId</span></span>
<span data-ttu-id="8a9aa-112">Указывает идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="8a9aa-113">-Context</span><span class="sxs-lookup"><span data-stu-id="8a9aa-113">-Context</span></span>
<span data-ttu-id="8a9aa-114">Указывает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="8a9aa-115">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="8a9aa-115">-OperationId</span></span>
<span data-ttu-id="8a9aa-116">Задает идентификатор операции API.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-116">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="8a9aa-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a9aa-117">-PassThru</span></span>
<span data-ttu-id="8a9aa-118">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="8a9aa-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a9aa-119">-Confirm</span></span>
<span data-ttu-id="8a9aa-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a9aa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a9aa-121">-WhatIf</span></span>
<span data-ttu-id="8a9aa-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a9aa-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a9aa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a9aa-124">-DefaultProfile</span></span>
<span data-ttu-id="8a9aa-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a9aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a9aa-126">CommonParameters</span></span>
<span data-ttu-id="8a9aa-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a9aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a9aa-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a9aa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a9aa-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a9aa-129">INPUTS</span></span>

## <span data-ttu-id="8a9aa-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a9aa-130">OUTPUTS</span></span>

### <span data-ttu-id="8a9aa-131">логических</span><span class="sxs-lookup"><span data-stu-id="8a9aa-131">bool</span></span>

## <span data-ttu-id="8a9aa-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a9aa-132">NOTES</span></span>

## <span data-ttu-id="8a9aa-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a9aa-133">RELATED LINKS</span></span>

[<span data-ttu-id="8a9aa-134">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8a9aa-134">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="8a9aa-135">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8a9aa-135">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="8a9aa-136">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="8a9aa-136">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


