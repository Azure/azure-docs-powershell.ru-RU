---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: efba6588697e34b371622eaa8a5f9a3c349d9ec0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077887"
---
# <span data-ttu-id="e7ac1-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e7ac1-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="e7ac1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ac1-103">Повторное создание ключа учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e7ac1-103">Regenerates an account key.</span></span>

## <span data-ttu-id="e7ac1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7ac1-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7ac1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7ac1-105">DESCRIPTION</span></span>
<span data-ttu-id="e7ac1-106">Командлет **New-AzCognitiveServicesAccountKey** заново создает ключ API для учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="e7ac1-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="e7ac1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7ac1-107">EXAMPLES</span></span>

### <span data-ttu-id="e7ac1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7ac1-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="e7ac1-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7ac1-109">PARAMETERS</span></span>

### <span data-ttu-id="e7ac1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ac1-110">-DefaultProfile</span></span>
<span data-ttu-id="e7ac1-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e7ac1-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7ac1-112">-Force</span><span class="sxs-lookup"><span data-stu-id="e7ac1-112">-Force</span></span>
<span data-ttu-id="e7ac1-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e7ac1-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e7ac1-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e7ac1-114">-KeyName</span></span>
<span data-ttu-id="e7ac1-115">Задает имя ключа, который нужно повторно создать.</span><span class="sxs-lookup"><span data-stu-id="e7ac1-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="e7ac1-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e7ac1-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e7ac1-117">Key1</span><span class="sxs-lookup"><span data-stu-id="e7ac1-117">Key1</span></span>
- <span data-ttu-id="e7ac1-118">Key2</span><span class="sxs-lookup"><span data-stu-id="e7ac1-118">Key2</span></span>

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

### <span data-ttu-id="e7ac1-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e7ac1-119">-Name</span></span>
<span data-ttu-id="e7ac1-120">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e7ac1-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="e7ac1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7ac1-121">-ResourceGroupName</span></span>
<span data-ttu-id="e7ac1-122">Указывает имя группы ресурсов, которой назначена эта учетная запись.</span><span class="sxs-lookup"><span data-stu-id="e7ac1-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="e7ac1-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7ac1-123">-Confirm</span></span>
<span data-ttu-id="e7ac1-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e7ac1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7ac1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7ac1-125">-WhatIf</span></span>
<span data-ttu-id="e7ac1-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e7ac1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7ac1-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e7ac1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7ac1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ac1-128">CommonParameters</span></span>
<span data-ttu-id="e7ac1-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7ac1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ac1-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7ac1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ac1-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7ac1-131">INPUTS</span></span>

### <span data-ttu-id="e7ac1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e7ac1-132">System.String</span></span>

### <span data-ttu-id="e7ac1-133">Microsoft. Azure. Management. CognitiveServices. Models. KeyName</span><span class="sxs-lookup"><span data-stu-id="e7ac1-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="e7ac1-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7ac1-134">OUTPUTS</span></span>

### <span data-ttu-id="e7ac1-135">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e7ac1-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="e7ac1-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7ac1-136">NOTES</span></span>

## <span data-ttu-id="e7ac1-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7ac1-137">RELATED LINKS</span></span>

[<span data-ttu-id="e7ac1-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e7ac1-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


