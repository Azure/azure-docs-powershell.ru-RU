---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: 5a46e75f7ce7b0639de015de975c321c9d5c1ed6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558020"
---
# <span data-ttu-id="7de45-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="7de45-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="7de45-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7de45-102">SYNOPSIS</span></span>
<span data-ttu-id="7de45-103">Удаляет службу управления API.</span><span class="sxs-lookup"><span data-stu-id="7de45-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7de45-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7de45-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7de45-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7de45-105">DESCRIPTION</span></span>
<span data-ttu-id="7de45-106">Командлет **Remove-AzureRmApiManagement** Удаляет службу управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="7de45-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="7de45-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7de45-107">EXAMPLES</span></span>

### <span data-ttu-id="7de45-108">Пример 1: Удаление службы управления API</span><span class="sxs-lookup"><span data-stu-id="7de45-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="7de45-109">Эта команда удаляет службу управления API с именем ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="7de45-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="7de45-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7de45-110">PARAMETERS</span></span>

### <span data-ttu-id="7de45-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7de45-111">-Name</span></span>
<span data-ttu-id="7de45-112">Указывает имя развертывания управления API, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7de45-112">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7de45-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7de45-113">-PassThru</span></span>
<span data-ttu-id="7de45-114">Указывает на то, что этот командлет возвращает значение $True, если операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7de45-114">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de45-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7de45-115">-ResourceGroupName</span></span>
<span data-ttu-id="7de45-116">Указывает имя группы ресурсов, в которой находится развертывание управления API.</span><span class="sxs-lookup"><span data-stu-id="7de45-116">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="7de45-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7de45-117">-Confirm</span></span>
<span data-ttu-id="7de45-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7de45-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7de45-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7de45-119">-WhatIf</span></span>
<span data-ttu-id="7de45-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7de45-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7de45-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7de45-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7de45-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de45-122">-DefaultProfile</span></span>
<span data-ttu-id="7de45-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7de45-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7de45-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de45-124">CommonParameters</span></span>
<span data-ttu-id="7de45-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7de45-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de45-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7de45-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de45-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7de45-127">INPUTS</span></span>

## <span data-ttu-id="7de45-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7de45-128">OUTPUTS</span></span>

### <span data-ttu-id="7de45-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7de45-129">System.Boolean</span></span>

## <span data-ttu-id="7de45-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="7de45-130">NOTES</span></span>

## <span data-ttu-id="7de45-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7de45-131">RELATED LINKS</span></span>

[<span data-ttu-id="7de45-132">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="7de45-132">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="7de45-133">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="7de45-133">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="7de45-134">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="7de45-134">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="7de45-135">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="7de45-135">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


