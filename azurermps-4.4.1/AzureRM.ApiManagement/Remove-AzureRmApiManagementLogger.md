---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 3c36d0b21b1fdda1282a1184f90728e827515195
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560576"
---
# <span data-ttu-id="0987b-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0987b-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="0987b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0987b-102">SYNOPSIS</span></span>
<span data-ttu-id="0987b-103">Удаляет средство ведения журнала управления API.</span><span class="sxs-lookup"><span data-stu-id="0987b-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0987b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0987b-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0987b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0987b-105">DESCRIPTION</span></span>
<span data-ttu-id="0987b-106">Командлет **Remove-AzureRmApiManagementLogger** удаляет **средство ведения журнала** управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="0987b-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="0987b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0987b-107">EXAMPLES</span></span>

### <span data-ttu-id="0987b-108">Пример 1: удаление средства ведения журнала</span><span class="sxs-lookup"><span data-stu-id="0987b-108">Example 1: Remove a logger</span></span>
```
PS C:\>Remove-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="0987b-109">Эта команда удаляет средство ведения журнала с ИДЕНТИФИКАТОРом Logger123.</span><span class="sxs-lookup"><span data-stu-id="0987b-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="0987b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0987b-110">PARAMETERS</span></span>

### <span data-ttu-id="0987b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="0987b-111">-Context</span></span>
<span data-ttu-id="0987b-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0987b-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0987b-113">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="0987b-113">-LoggerId</span></span>
<span data-ttu-id="0987b-114">Указывает идентификатор средства ведения журнала, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="0987b-114">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="0987b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0987b-115">-PassThru</span></span>
<span data-ttu-id="0987b-116">Указывает на то, что этот командлет возвращает значение $True, если операция выполнена успешно или $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0987b-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="0987b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0987b-117">-Confirm</span></span>
<span data-ttu-id="0987b-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0987b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0987b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0987b-119">-WhatIf</span></span>
<span data-ttu-id="0987b-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0987b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0987b-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0987b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0987b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0987b-122">-DefaultProfile</span></span>
<span data-ttu-id="0987b-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0987b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0987b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0987b-124">CommonParameters</span></span>
<span data-ttu-id="0987b-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0987b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0987b-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0987b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0987b-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0987b-127">INPUTS</span></span>

## <span data-ttu-id="0987b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0987b-128">OUTPUTS</span></span>

### <span data-ttu-id="0987b-129">Значением</span><span class="sxs-lookup"><span data-stu-id="0987b-129">Boolean</span></span>

## <span data-ttu-id="0987b-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="0987b-130">NOTES</span></span>

## <span data-ttu-id="0987b-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0987b-131">RELATED LINKS</span></span>

[<span data-ttu-id="0987b-132">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0987b-132">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="0987b-133">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0987b-133">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="0987b-134">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0987b-134">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


