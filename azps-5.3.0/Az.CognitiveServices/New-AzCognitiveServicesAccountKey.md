---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: efba6588697e34b371622eaa8a5f9a3c349d9ec0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519680"
---
# <span data-ttu-id="e7d4d-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e7d4d-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="e7d4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d4d-103">Повторное сгенерирует ключ учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e7d4d-103">Regenerates an account key.</span></span>

## <span data-ttu-id="e7d4d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e7d4d-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7d4d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7d4d-105">DESCRIPTION</span></span>
<span data-ttu-id="e7d4d-106">Cmdlet **New-AzCognitiveServicesAccountKey** повторно сгенерирует ключ API для учетной записи службы восприятия.</span><span class="sxs-lookup"><span data-stu-id="e7d4d-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="e7d4d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e7d4d-107">EXAMPLES</span></span>

### <span data-ttu-id="e7d4d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7d4d-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="e7d4d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7d4d-109">PARAMETERS</span></span>

### <span data-ttu-id="e7d4d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d4d-110">-DefaultProfile</span></span>
<span data-ttu-id="e7d4d-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e7d4d-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7d4d-112">-Force</span><span class="sxs-lookup"><span data-stu-id="e7d4d-112">-Force</span></span>
<span data-ttu-id="e7d4d-113">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e7d4d-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e7d4d-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e7d4d-114">-KeyName</span></span>
<span data-ttu-id="e7d4d-115">Указывает имя ключа, который нужно сгенерировать.</span><span class="sxs-lookup"><span data-stu-id="e7d4d-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="e7d4d-116">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="e7d4d-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e7d4d-117">Ключ1</span><span class="sxs-lookup"><span data-stu-id="e7d4d-117">Key1</span></span>
- <span data-ttu-id="e7d4d-118">Ключ2</span><span class="sxs-lookup"><span data-stu-id="e7d4d-118">Key2</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.KeyName
Parameter Sets: (All)
Aliases:
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d4d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e7d4d-119">-Name</span></span>
<span data-ttu-id="e7d4d-120">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e7d4d-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="e7d4d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7d4d-121">-ResourceGroupName</span></span>
<span data-ttu-id="e7d4d-122">Имя группы ресурсов, назначенной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e7d4d-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="e7d4d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7d4d-123">-Confirm</span></span>
<span data-ttu-id="e7d4d-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e7d4d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7d4d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7d4d-125">-WhatIf</span></span>
<span data-ttu-id="e7d4d-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7d4d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7d4d-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e7d4d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7d4d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d4d-128">CommonParameters</span></span>
<span data-ttu-id="e7d4d-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7d4d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d4d-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7d4d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d4d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7d4d-131">INPUTS</span></span>

### <span data-ttu-id="e7d4d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e7d4d-132">System.String</span></span>

### <span data-ttu-id="e7d4d-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span><span class="sxs-lookup"><span data-stu-id="e7d4d-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="e7d4d-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e7d4d-134">OUTPUTS</span></span>

### <span data-ttu-id="e7d4d-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e7d4d-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="e7d4d-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e7d4d-136">NOTES</span></span>

## <span data-ttu-id="e7d4d-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7d4d-137">RELATED LINKS</span></span>

[<span data-ttu-id="e7d4d-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e7d4d-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


