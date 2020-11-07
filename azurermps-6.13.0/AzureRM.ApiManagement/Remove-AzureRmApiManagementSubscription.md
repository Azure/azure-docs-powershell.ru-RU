---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 09a0af4685701de60fc85c1572b492e7582ff71e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733506"
---
# <span data-ttu-id="599e8-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="599e8-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="599e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="599e8-102">SYNOPSIS</span></span>
<span data-ttu-id="599e8-103">Удаление существующей подписки.</span><span class="sxs-lookup"><span data-stu-id="599e8-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="599e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="599e8-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="599e8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="599e8-105">DESCRIPTION</span></span>
<span data-ttu-id="599e8-106">Командлет **Remove-AzureRmApiManagementSubscription** удаляет существующую подписку.</span><span class="sxs-lookup"><span data-stu-id="599e8-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="599e8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="599e8-107">EXAMPLES</span></span>

### <span data-ttu-id="599e8-108">Пример 1: Удаление подписки</span><span class="sxs-lookup"><span data-stu-id="599e8-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="599e8-109">Эта команда удаляет существующую подписку.</span><span class="sxs-lookup"><span data-stu-id="599e8-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="599e8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="599e8-110">PARAMETERS</span></span>

### <span data-ttu-id="599e8-111">-Context</span><span class="sxs-lookup"><span data-stu-id="599e8-111">-Context</span></span>
<span data-ttu-id="599e8-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="599e8-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="599e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="599e8-113">-DefaultProfile</span></span>
<span data-ttu-id="599e8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="599e8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="599e8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="599e8-115">-PassThru</span></span>
<span data-ttu-id="599e8-116">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $false, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="599e8-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="599e8-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="599e8-117">-SubscriptionId</span></span>
<span data-ttu-id="599e8-118">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="599e8-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="599e8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="599e8-119">-Confirm</span></span>
<span data-ttu-id="599e8-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="599e8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="599e8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="599e8-121">-WhatIf</span></span>
<span data-ttu-id="599e8-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="599e8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="599e8-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="599e8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="599e8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="599e8-124">CommonParameters</span></span>
<span data-ttu-id="599e8-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="599e8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="599e8-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="599e8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="599e8-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="599e8-127">INPUTS</span></span>

### <span data-ttu-id="599e8-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="599e8-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="599e8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="599e8-129">System.String</span></span>

### <span data-ttu-id="599e8-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="599e8-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="599e8-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="599e8-131">OUTPUTS</span></span>

### <span data-ttu-id="599e8-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="599e8-132">System.Boolean</span></span>

## <span data-ttu-id="599e8-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="599e8-133">NOTES</span></span>

## <span data-ttu-id="599e8-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="599e8-134">RELATED LINKS</span></span>

[<span data-ttu-id="599e8-135">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="599e8-135">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="599e8-136">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="599e8-136">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="599e8-137">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="599e8-137">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


