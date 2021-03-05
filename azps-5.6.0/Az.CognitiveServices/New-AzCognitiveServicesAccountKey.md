---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 22e4f7e115016930e3745e5ce317a3deaa84ad71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981187"
---
# <span data-ttu-id="83342-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="83342-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="83342-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83342-102">SYNOPSIS</span></span>
<span data-ttu-id="83342-103">Повторное сгенерирует ключ учетной записи.</span><span class="sxs-lookup"><span data-stu-id="83342-103">Regenerates an account key.</span></span>

## <span data-ttu-id="83342-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="83342-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83342-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83342-105">DESCRIPTION</span></span>
<span data-ttu-id="83342-106">Cmdlet **New-AzCognitiveServicesAccountKey** повторно сгенерирует ключ API для учетной записи службы когнитивных функций.</span><span class="sxs-lookup"><span data-stu-id="83342-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="83342-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="83342-107">EXAMPLES</span></span>

### <span data-ttu-id="83342-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="83342-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="83342-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83342-109">PARAMETERS</span></span>

### <span data-ttu-id="83342-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83342-110">-DefaultProfile</span></span>
<span data-ttu-id="83342-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="83342-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83342-112">-Force</span><span class="sxs-lookup"><span data-stu-id="83342-112">-Force</span></span>
<span data-ttu-id="83342-113">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="83342-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="83342-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="83342-114">-KeyName</span></span>
<span data-ttu-id="83342-115">Имя ключа, который нужно сгенерировать.</span><span class="sxs-lookup"><span data-stu-id="83342-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="83342-116">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="83342-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="83342-117">Ключ1</span><span class="sxs-lookup"><span data-stu-id="83342-117">Key1</span></span>
- <span data-ttu-id="83342-118">Ключ2</span><span class="sxs-lookup"><span data-stu-id="83342-118">Key2</span></span>

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

### <span data-ttu-id="83342-119">-Name</span><span class="sxs-lookup"><span data-stu-id="83342-119">-Name</span></span>
<span data-ttu-id="83342-120">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="83342-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="83342-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83342-121">-ResourceGroupName</span></span>
<span data-ttu-id="83342-122">Имя группы ресурсов, назначенной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="83342-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="83342-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83342-123">-Confirm</span></span>
<span data-ttu-id="83342-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83342-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83342-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83342-125">-WhatIf</span></span>
<span data-ttu-id="83342-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83342-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83342-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="83342-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83342-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83342-128">CommonParameters</span></span>
<span data-ttu-id="83342-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83342-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83342-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83342-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83342-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83342-131">INPUTS</span></span>

### <span data-ttu-id="83342-132">System.String</span><span class="sxs-lookup"><span data-stu-id="83342-132">System.String</span></span>

### <span data-ttu-id="83342-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span><span class="sxs-lookup"><span data-stu-id="83342-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="83342-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="83342-134">OUTPUTS</span></span>

### <span data-ttu-id="83342-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="83342-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="83342-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="83342-136">NOTES</span></span>

## <span data-ttu-id="83342-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83342-137">RELATED LINKS</span></span>

[<span data-ttu-id="83342-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="83342-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


