---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: 1069365bb04cdf9a6d873e6fa86c61619b6d0dab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239026"
---
# <span data-ttu-id="a39a9-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a39a9-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="a39a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a39a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a39a9-103">Удаляет учетную запись когнитивных служб.</span><span class="sxs-lookup"><span data-stu-id="a39a9-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="a39a9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a39a9-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a39a9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a39a9-105">DESCRIPTION</span></span>
<span data-ttu-id="a39a9-106">С **помощью cmdlet Remove-AzCognitiveServicesAccount** можно удалить указанную учетную запись службы восприятия.</span><span class="sxs-lookup"><span data-stu-id="a39a9-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="a39a9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a39a9-107">EXAMPLES</span></span>

### <span data-ttu-id="a39a9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a39a9-108">Example 1</span></span>
<span data-ttu-id="a39a9-109">Эта команда ничего не возвращает.</span><span class="sxs-lookup"><span data-stu-id="a39a9-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="a39a9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a39a9-110">PARAMETERS</span></span>

### <span data-ttu-id="a39a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a39a9-111">-DefaultProfile</span></span>
<span data-ttu-id="a39a9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a39a9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a39a9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a39a9-113">-Force</span></span>
<span data-ttu-id="a39a9-114">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a39a9-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a39a9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a39a9-115">-Name</span></span>
<span data-ttu-id="a39a9-116">Указывает имя учетной записи, которая нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a39a9-116">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="a39a9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a39a9-117">-ResourceGroupName</span></span>
<span data-ttu-id="a39a9-118">Указывает имя группы ресурсов, которая назначена учетной записи "Когнитивные услуги".</span><span class="sxs-lookup"><span data-stu-id="a39a9-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="a39a9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a39a9-119">-Confirm</span></span>
<span data-ttu-id="a39a9-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a39a9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a39a9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a39a9-121">-WhatIf</span></span>
<span data-ttu-id="a39a9-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a39a9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a39a9-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a39a9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a39a9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a39a9-124">CommonParameters</span></span>
<span data-ttu-id="a39a9-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a39a9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a39a9-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a39a9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a39a9-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a39a9-127">INPUTS</span></span>

### <span data-ttu-id="a39a9-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a39a9-128">System.String</span></span>

## <span data-ttu-id="a39a9-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a39a9-129">OUTPUTS</span></span>

### <span data-ttu-id="a39a9-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="a39a9-130">System.Void</span></span>

## <span data-ttu-id="a39a9-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a39a9-131">NOTES</span></span>

## <span data-ttu-id="a39a9-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a39a9-132">RELATED LINKS</span></span>

[<span data-ttu-id="a39a9-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a39a9-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="a39a9-134">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a39a9-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="a39a9-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a39a9-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


