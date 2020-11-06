---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: 197b1605d178c0aaa1c3f96580cb295306910232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568657"
---
# <span data-ttu-id="90cc7-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="90cc7-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="90cc7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90cc7-102">SYNOPSIS</span></span>
<span data-ttu-id="90cc7-103">Удаляет службу управления API.</span><span class="sxs-lookup"><span data-stu-id="90cc7-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90cc7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90cc7-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90cc7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90cc7-105">DESCRIPTION</span></span>
<span data-ttu-id="90cc7-106">Командлет **Remove-AzureRmApiManagement** Удаляет службу управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="90cc7-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="90cc7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90cc7-107">EXAMPLES</span></span>

### <span data-ttu-id="90cc7-108">Пример 1: Удаление службы управления API</span><span class="sxs-lookup"><span data-stu-id="90cc7-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="90cc7-109">Эта команда удаляет службу управления API с именем ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="90cc7-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="90cc7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90cc7-110">PARAMETERS</span></span>

### <span data-ttu-id="90cc7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90cc7-111">-DefaultProfile</span></span>
<span data-ttu-id="90cc7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90cc7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90cc7-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="90cc7-113">-Name</span></span>
<span data-ttu-id="90cc7-114">Указывает имя развертывания управления API, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="90cc7-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90cc7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90cc7-115">-PassThru</span></span>
<span data-ttu-id="90cc7-116">Указывает на то, что этот командлет возвращает значение $True, если операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="90cc7-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90cc7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90cc7-117">-ResourceGroupName</span></span>
<span data-ttu-id="90cc7-118">Указывает имя группы ресурсов, в которой находится развертывание управления API.</span><span class="sxs-lookup"><span data-stu-id="90cc7-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90cc7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90cc7-119">-Confirm</span></span>
<span data-ttu-id="90cc7-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="90cc7-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90cc7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90cc7-121">-WhatIf</span></span>
<span data-ttu-id="90cc7-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="90cc7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90cc7-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="90cc7-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90cc7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90cc7-124">CommonParameters</span></span>
<span data-ttu-id="90cc7-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90cc7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90cc7-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90cc7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90cc7-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90cc7-127">INPUTS</span></span>

### <span data-ttu-id="90cc7-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="90cc7-128">None</span></span>
<span data-ttu-id="90cc7-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="90cc7-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="90cc7-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90cc7-130">OUTPUTS</span></span>

### <span data-ttu-id="90cc7-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90cc7-131">System.Boolean</span></span>

## <span data-ttu-id="90cc7-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="90cc7-132">NOTES</span></span>

## <span data-ttu-id="90cc7-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90cc7-133">RELATED LINKS</span></span>

[<span data-ttu-id="90cc7-134">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="90cc7-134">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="90cc7-135">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="90cc7-135">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="90cc7-136">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="90cc7-136">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="90cc7-137">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="90cc7-137">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


