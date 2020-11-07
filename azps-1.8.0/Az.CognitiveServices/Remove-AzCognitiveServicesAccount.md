---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: ad3c5359d80f3133e6bb48ea73c1d6a93501288a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731386"
---
# <span data-ttu-id="097a1-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="097a1-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="097a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="097a1-102">SYNOPSIS</span></span>
<span data-ttu-id="097a1-103">Удаление учетной записи службы для восприятия.</span><span class="sxs-lookup"><span data-stu-id="097a1-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="097a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="097a1-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="097a1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="097a1-105">DESCRIPTION</span></span>
<span data-ttu-id="097a1-106">Командлет **Remove-AzCognitiveServicesAccount** удаляет указанную учетную запись службы.</span><span class="sxs-lookup"><span data-stu-id="097a1-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="097a1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="097a1-107">EXAMPLES</span></span>

### <span data-ttu-id="097a1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="097a1-108">Example 1</span></span>
<span data-ttu-id="097a1-109">Эта команда ничего не возвращает.</span><span class="sxs-lookup"><span data-stu-id="097a1-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="097a1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="097a1-110">PARAMETERS</span></span>

### <span data-ttu-id="097a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="097a1-111">-DefaultProfile</span></span>
<span data-ttu-id="097a1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="097a1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="097a1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="097a1-113">-Force</span></span>
<span data-ttu-id="097a1-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="097a1-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="097a1-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="097a1-115">-Name</span></span>
<span data-ttu-id="097a1-116">Указывает имя учетной записи, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="097a1-116">Specifies the name of the account to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="097a1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="097a1-117">-ResourceGroupName</span></span>
<span data-ttu-id="097a1-118">Указывает имя группы ресурсов, которой назначена учетная запись службы.</span><span class="sxs-lookup"><span data-stu-id="097a1-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="097a1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="097a1-119">-Confirm</span></span>
<span data-ttu-id="097a1-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="097a1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="097a1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="097a1-121">-WhatIf</span></span>
<span data-ttu-id="097a1-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="097a1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="097a1-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="097a1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="097a1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="097a1-124">CommonParameters</span></span>
<span data-ttu-id="097a1-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="097a1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="097a1-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="097a1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="097a1-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="097a1-127">INPUTS</span></span>

### <span data-ttu-id="097a1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="097a1-128">System.String</span></span>

## <span data-ttu-id="097a1-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="097a1-129">OUTPUTS</span></span>

### <span data-ttu-id="097a1-130">System. void</span><span class="sxs-lookup"><span data-stu-id="097a1-130">System.Void</span></span>

## <span data-ttu-id="097a1-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="097a1-131">NOTES</span></span>

## <span data-ttu-id="097a1-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="097a1-132">RELATED LINKS</span></span>

[<span data-ttu-id="097a1-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="097a1-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="097a1-134">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="097a1-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="097a1-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="097a1-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


