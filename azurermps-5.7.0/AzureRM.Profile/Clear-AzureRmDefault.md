---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
ms.openlocfilehash: 4f3a463f8ae03dcbefaf9588ca196f01955070ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557271"
---
# <span data-ttu-id="3b6bd-101">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="3b6bd-101">Clear-AzureRmDefault</span></span>

## <span data-ttu-id="3b6bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b6bd-102">SYNOPSIS</span></span>
<span data-ttu-id="3b6bd-103">Очищает значения по умолчанию, заданные пользователем в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="3b6bd-103">Clears the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b6bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b6bd-104">SYNTAX</span></span>

```
Clear-AzureRmDefault [-ResourceGroup] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b6bd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b6bd-105">DESCRIPTION</span></span>
<span data-ttu-id="3b6bd-106">Командлет Clear-AzureRmDefault удаляет значения по умолчанию, заданные пользователем, в зависимости от параметров переключателей, указанных пользователем.</span><span class="sxs-lookup"><span data-stu-id="3b6bd-106">The Clear-AzureRmDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="3b6bd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b6bd-107">EXAMPLES</span></span>

### <span data-ttu-id="3b6bd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3b6bd-108">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault
```

<span data-ttu-id="3b6bd-109">Эта команда удаляет все значения по умолчанию, заданные пользователем в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="3b6bd-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="3b6bd-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3b6bd-110">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault -ResourceGroup
```

<span data-ttu-id="3b6bd-111">Эта команда удаляет группу ресурсов по умолчанию, установленную пользователем в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="3b6bd-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="3b6bd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b6bd-112">PARAMETERS</span></span>

### <span data-ttu-id="3b6bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b6bd-113">-DefaultProfile</span></span>
<span data-ttu-id="3b6bd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b6bd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b6bd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3b6bd-115">-Force</span></span>
<span data-ttu-id="3b6bd-116">Удаление всех значений по умолчанию, если не задано значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3b6bd-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="3b6bd-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b6bd-117">-PassThru</span></span>
<span data-ttu-id="3b6bd-118">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="3b6bd-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3b6bd-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3b6bd-119">-ResourceGroup</span></span>
<span data-ttu-id="3b6bd-120">Очистить группу ресурсов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3b6bd-120">Clear Default Resource Group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b6bd-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b6bd-121">-Confirm</span></span>
<span data-ttu-id="3b6bd-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3b6bd-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6bd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b6bd-123">-WhatIf</span></span>
<span data-ttu-id="3b6bd-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3b6bd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b6bd-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3b6bd-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b6bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b6bd-126">CommonParameters</span></span>
<span data-ttu-id="3b6bd-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b6bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b6bd-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b6bd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b6bd-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b6bd-129">INPUTS</span></span>

### <span data-ttu-id="3b6bd-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3b6bd-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3b6bd-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b6bd-131">OUTPUTS</span></span>

### <span data-ttu-id="3b6bd-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="3b6bd-132">System.Object</span></span>

## <span data-ttu-id="3b6bd-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b6bd-133">NOTES</span></span>

## <span data-ttu-id="3b6bd-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b6bd-134">RELATED LINKS</span></span>

