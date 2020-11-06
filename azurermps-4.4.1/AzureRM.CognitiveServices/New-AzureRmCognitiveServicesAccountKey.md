---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 345e7c6365a66abde5f350f20f614d4d6c94b1b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569699"
---
# <span data-ttu-id="8f474-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="8f474-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="8f474-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f474-102">SYNOPSIS</span></span>
<span data-ttu-id="8f474-103">Повторное создание ключа учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8f474-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f474-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f474-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f474-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f474-105">DESCRIPTION</span></span>
<span data-ttu-id="8f474-106">Командлет **New-AzureRmCognitiveServicesAccountKey** заново создает ключ API для учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="8f474-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="8f474-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f474-107">EXAMPLES</span></span>

## <span data-ttu-id="8f474-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f474-108">PARAMETERS</span></span>

### <span data-ttu-id="8f474-109">-Force</span><span class="sxs-lookup"><span data-stu-id="8f474-109">-Force</span></span>
<span data-ttu-id="8f474-110">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8f474-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8f474-111">-KeyName</span><span class="sxs-lookup"><span data-stu-id="8f474-111">-KeyName</span></span>
<span data-ttu-id="8f474-112">Задает имя ключа, который нужно повторно создать.</span><span class="sxs-lookup"><span data-stu-id="8f474-112">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="8f474-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8f474-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8f474-114">Key1</span><span class="sxs-lookup"><span data-stu-id="8f474-114">Key1</span></span>
- <span data-ttu-id="8f474-115">Key2</span><span class="sxs-lookup"><span data-stu-id="8f474-115">Key2</span></span>

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

### <span data-ttu-id="8f474-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f474-116">-Name</span></span>
<span data-ttu-id="8f474-117">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8f474-117">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="8f474-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f474-118">-ResourceGroupName</span></span>
<span data-ttu-id="8f474-119">Указывает имя группы ресурсов, которой назначена эта учетная запись.</span><span class="sxs-lookup"><span data-stu-id="8f474-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="8f474-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f474-120">-Confirm</span></span>
<span data-ttu-id="8f474-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8f474-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f474-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f474-122">-WhatIf</span></span>
<span data-ttu-id="8f474-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8f474-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f474-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8f474-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f474-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f474-125">-DefaultProfile</span></span>
<span data-ttu-id="8f474-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f474-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f474-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f474-127">CommonParameters</span></span>
<span data-ttu-id="8f474-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f474-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f474-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f474-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f474-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f474-130">INPUTS</span></span>

## <span data-ttu-id="8f474-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f474-131">OUTPUTS</span></span>

### <span data-ttu-id="8f474-132">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8f474-132">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="8f474-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f474-133">NOTES</span></span>

## <span data-ttu-id="8f474-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f474-134">RELATED LINKS</span></span>

[<span data-ttu-id="8f474-135">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="8f474-135">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


