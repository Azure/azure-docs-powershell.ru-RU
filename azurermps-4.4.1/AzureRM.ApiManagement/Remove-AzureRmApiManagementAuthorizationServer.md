---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 16a48b6f945aac8ef287ff612d64da1273add521
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558015"
---
# <span data-ttu-id="c9d48-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c9d48-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="c9d48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9d48-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d48-103">Удаление сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="c9d48-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9d48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9d48-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9d48-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9d48-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d48-106">Командлет **Remove-AzureRmApiManagementAuthorizationServer** удаляет сервер авторизации управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="c9d48-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="c9d48-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9d48-107">EXAMPLES</span></span>

## <span data-ttu-id="c9d48-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9d48-108">PARAMETERS</span></span>

### <span data-ttu-id="c9d48-109">-Context</span><span class="sxs-lookup"><span data-stu-id="c9d48-109">-Context</span></span>
<span data-ttu-id="c9d48-110">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c9d48-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c9d48-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9d48-111">-PassThru</span></span>
<span data-ttu-id="c9d48-112">PassThru</span><span class="sxs-lookup"><span data-stu-id="c9d48-112">passthru</span></span>

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

### <span data-ttu-id="c9d48-113">-ServerId</span><span class="sxs-lookup"><span data-stu-id="c9d48-113">-ServerId</span></span>
<span data-ttu-id="c9d48-114">Указывает идентификатор сервера авторизации, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c9d48-114">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="c9d48-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9d48-115">-Confirm</span></span>
<span data-ttu-id="c9d48-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c9d48-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9d48-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9d48-117">-WhatIf</span></span>
<span data-ttu-id="c9d48-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c9d48-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9d48-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c9d48-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9d48-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d48-120">-DefaultProfile</span></span>
<span data-ttu-id="c9d48-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9d48-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9d48-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d48-122">CommonParameters</span></span>
<span data-ttu-id="c9d48-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9d48-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d48-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d48-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d48-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9d48-125">INPUTS</span></span>

## <span data-ttu-id="c9d48-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9d48-126">OUTPUTS</span></span>

### <span data-ttu-id="c9d48-127">Значением</span><span class="sxs-lookup"><span data-stu-id="c9d48-127">Boolean</span></span>

## <span data-ttu-id="c9d48-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9d48-128">NOTES</span></span>

## <span data-ttu-id="c9d48-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9d48-129">RELATED LINKS</span></span>

[<span data-ttu-id="c9d48-130">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c9d48-130">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="c9d48-131">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c9d48-131">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="c9d48-132">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c9d48-132">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


