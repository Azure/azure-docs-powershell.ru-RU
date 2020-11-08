---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: 1069365bb04cdf9a6d873e6fa86c61619b6d0dab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077886"
---
# <span data-ttu-id="7b7e2-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7b7e2-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="7b7e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b7e2-102">SYNOPSIS</span></span>
<span data-ttu-id="7b7e2-103">Удаление учетной записи службы для восприятия.</span><span class="sxs-lookup"><span data-stu-id="7b7e2-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="7b7e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b7e2-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b7e2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b7e2-105">DESCRIPTION</span></span>
<span data-ttu-id="7b7e2-106">Командлет **Remove-AzCognitiveServicesAccount** удаляет указанную учетную запись службы.</span><span class="sxs-lookup"><span data-stu-id="7b7e2-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="7b7e2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b7e2-107">EXAMPLES</span></span>

### <span data-ttu-id="7b7e2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7b7e2-108">Example 1</span></span>
<span data-ttu-id="7b7e2-109">Эта команда ничего не возвращает.</span><span class="sxs-lookup"><span data-stu-id="7b7e2-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="7b7e2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b7e2-110">PARAMETERS</span></span>

### <span data-ttu-id="7b7e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b7e2-111">-DefaultProfile</span></span>
<span data-ttu-id="7b7e2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7b7e2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b7e2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7b7e2-113">-Force</span></span>
<span data-ttu-id="7b7e2-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7b7e2-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7b7e2-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7b7e2-115">-Name</span></span>
<span data-ttu-id="7b7e2-116">Указывает имя учетной записи, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7b7e2-116">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="7b7e2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b7e2-117">-ResourceGroupName</span></span>
<span data-ttu-id="7b7e2-118">Указывает имя группы ресурсов, которой назначена учетная запись службы.</span><span class="sxs-lookup"><span data-stu-id="7b7e2-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="7b7e2-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b7e2-119">-Confirm</span></span>
<span data-ttu-id="7b7e2-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7b7e2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b7e2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b7e2-121">-WhatIf</span></span>
<span data-ttu-id="7b7e2-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7b7e2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b7e2-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7b7e2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b7e2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b7e2-124">CommonParameters</span></span>
<span data-ttu-id="7b7e2-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b7e2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b7e2-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b7e2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b7e2-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b7e2-127">INPUTS</span></span>

### <span data-ttu-id="7b7e2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7b7e2-128">System.String</span></span>

## <span data-ttu-id="7b7e2-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b7e2-129">OUTPUTS</span></span>

### <span data-ttu-id="7b7e2-130">System. void</span><span class="sxs-lookup"><span data-stu-id="7b7e2-130">System.Void</span></span>

## <span data-ttu-id="7b7e2-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b7e2-131">NOTES</span></span>

## <span data-ttu-id="7b7e2-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b7e2-132">RELATED LINKS</span></span>

[<span data-ttu-id="7b7e2-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7b7e2-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="7b7e2-134">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7b7e2-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="7b7e2-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7b7e2-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


