---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: 1069365bb04cdf9a6d873e6fa86c61619b6d0dab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064771"
---
# <span data-ttu-id="9a4ef-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9a4ef-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="9a4ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a4ef-102">SYNOPSIS</span></span>
<span data-ttu-id="9a4ef-103">Удаление учетной записи службы для восприятия.</span><span class="sxs-lookup"><span data-stu-id="9a4ef-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="9a4ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a4ef-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a4ef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a4ef-105">DESCRIPTION</span></span>
<span data-ttu-id="9a4ef-106">Командлет **Remove-AzCognitiveServicesAccount** удаляет указанную учетную запись службы.</span><span class="sxs-lookup"><span data-stu-id="9a4ef-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="9a4ef-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a4ef-107">EXAMPLES</span></span>

### <span data-ttu-id="9a4ef-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9a4ef-108">Example 1</span></span>
<span data-ttu-id="9a4ef-109">Эта команда ничего не возвращает.</span><span class="sxs-lookup"><span data-stu-id="9a4ef-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="9a4ef-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a4ef-110">PARAMETERS</span></span>

### <span data-ttu-id="9a4ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a4ef-111">-DefaultProfile</span></span>
<span data-ttu-id="9a4ef-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9a4ef-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a4ef-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9a4ef-113">-Force</span></span>
<span data-ttu-id="9a4ef-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9a4ef-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9a4ef-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9a4ef-115">-Name</span></span>
<span data-ttu-id="9a4ef-116">Указывает имя учетной записи, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9a4ef-116">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="9a4ef-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a4ef-117">-ResourceGroupName</span></span>
<span data-ttu-id="9a4ef-118">Указывает имя группы ресурсов, которой назначена учетная запись службы.</span><span class="sxs-lookup"><span data-stu-id="9a4ef-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="9a4ef-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a4ef-119">-Confirm</span></span>
<span data-ttu-id="9a4ef-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9a4ef-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a4ef-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a4ef-121">-WhatIf</span></span>
<span data-ttu-id="9a4ef-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9a4ef-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a4ef-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9a4ef-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a4ef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a4ef-124">CommonParameters</span></span>
<span data-ttu-id="9a4ef-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a4ef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a4ef-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a4ef-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a4ef-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a4ef-127">INPUTS</span></span>

### <span data-ttu-id="9a4ef-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9a4ef-128">System.String</span></span>

## <span data-ttu-id="9a4ef-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a4ef-129">OUTPUTS</span></span>

### <span data-ttu-id="9a4ef-130">System. void</span><span class="sxs-lookup"><span data-stu-id="9a4ef-130">System.Void</span></span>

## <span data-ttu-id="9a4ef-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a4ef-131">NOTES</span></span>

## <span data-ttu-id="9a4ef-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a4ef-132">RELATED LINKS</span></span>

[<span data-ttu-id="9a4ef-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9a4ef-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="9a4ef-134">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9a4ef-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="9a4ef-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9a4ef-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


