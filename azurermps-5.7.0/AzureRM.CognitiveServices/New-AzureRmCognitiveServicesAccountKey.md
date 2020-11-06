---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 1c3ebaf3e95c1094b02b73505e471d13015721d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559224"
---
# <span data-ttu-id="cffb5-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="cffb5-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="cffb5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cffb5-102">SYNOPSIS</span></span>
<span data-ttu-id="cffb5-103">Повторное создание ключа учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cffb5-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cffb5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cffb5-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cffb5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cffb5-105">DESCRIPTION</span></span>
<span data-ttu-id="cffb5-106">Командлет **New-AzureRmCognitiveServicesAccountKey** заново создает ключ API для учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="cffb5-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="cffb5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cffb5-107">EXAMPLES</span></span>

## <span data-ttu-id="cffb5-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cffb5-108">PARAMETERS</span></span>

### <span data-ttu-id="cffb5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cffb5-109">-DefaultProfile</span></span>
<span data-ttu-id="cffb5-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cffb5-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cffb5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="cffb5-111">-Force</span></span>
<span data-ttu-id="cffb5-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="cffb5-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cffb5-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="cffb5-113">-KeyName</span></span>
<span data-ttu-id="cffb5-114">Задает имя ключа, который нужно повторно создать.</span><span class="sxs-lookup"><span data-stu-id="cffb5-114">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="cffb5-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cffb5-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cffb5-116">Key1</span><span class="sxs-lookup"><span data-stu-id="cffb5-116">Key1</span></span>
- <span data-ttu-id="cffb5-117">Key2</span><span class="sxs-lookup"><span data-stu-id="cffb5-117">Key2</span></span>

```yaml
Type: KeyName
Parameter Sets: (All)
Aliases: 
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffb5-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cffb5-118">-Name</span></span>
<span data-ttu-id="cffb5-119">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cffb5-119">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffb5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cffb5-120">-ResourceGroupName</span></span>
<span data-ttu-id="cffb5-121">Указывает имя группы ресурсов, которой назначена эта учетная запись.</span><span class="sxs-lookup"><span data-stu-id="cffb5-121">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffb5-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cffb5-122">-Confirm</span></span>
<span data-ttu-id="cffb5-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cffb5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cffb5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cffb5-124">-WhatIf</span></span>
<span data-ttu-id="cffb5-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cffb5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cffb5-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cffb5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cffb5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cffb5-127">CommonParameters</span></span>
<span data-ttu-id="cffb5-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cffb5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cffb5-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cffb5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cffb5-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cffb5-130">INPUTS</span></span>

### <span data-ttu-id="cffb5-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="cffb5-131">None</span></span>
<span data-ttu-id="cffb5-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="cffb5-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cffb5-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cffb5-133">OUTPUTS</span></span>

### <span data-ttu-id="cffb5-134">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cffb5-134">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="cffb5-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="cffb5-135">NOTES</span></span>

## <span data-ttu-id="cffb5-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cffb5-136">RELATED LINKS</span></span>

[<span data-ttu-id="cffb5-137">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="cffb5-137">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


