---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a31ee6979a73e4637e683a5b388f4265bf53d2a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568636"
---
# <span data-ttu-id="fa5cb-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fa5cb-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="fa5cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="fa5cb-103">Изменение учетной записи.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa5cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa5cb-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa5cb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa5cb-105">DESCRIPTION</span></span>
<span data-ttu-id="fa5cb-106">Командлет **Set-AzureRmCognitiveServicesAccount** изменяет SKU или теги указанной учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="fa5cb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa5cb-107">EXAMPLES</span></span>

## <span data-ttu-id="fa5cb-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa5cb-108">PARAMETERS</span></span>

### <span data-ttu-id="fa5cb-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa5cb-109">-DefaultProfile</span></span>
<span data-ttu-id="fa5cb-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fa5cb-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa5cb-111">-Force</span><span class="sxs-lookup"><span data-stu-id="fa5cb-111">-Force</span></span>
<span data-ttu-id="fa5cb-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fa5cb-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fa5cb-113">-Name</span></span>
<span data-ttu-id="fa5cb-114">Указывает имя учетной записи, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-114">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="fa5cb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa5cb-115">-ResourceGroupName</span></span>
<span data-ttu-id="fa5cb-116">Указывает имя группы ресурсов, которой назначена эта учетная запись.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-116">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="fa5cb-117">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fa5cb-117">-SkuName</span></span>
<span data-ttu-id="fa5cb-118">Указывает SKU для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-118">Specifies the SKU for the account.</span></span>
<span data-ttu-id="fa5cb-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fa5cb-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa5cb-120">F0 (бесплатный уровень)</span><span class="sxs-lookup"><span data-stu-id="fa5cb-120">F0 (free tier)</span></span>
- <span data-ttu-id="fa5cb-121">S0</span><span class="sxs-lookup"><span data-stu-id="fa5cb-121">S0</span></span>
- <span data-ttu-id="fa5cb-122">Состояний</span><span class="sxs-lookup"><span data-stu-id="fa5cb-122">S1</span></span>
- <span data-ttu-id="fa5cb-123">S2</span><span class="sxs-lookup"><span data-stu-id="fa5cb-123">S2</span></span>
- <span data-ttu-id="fa5cb-124">Режима</span><span class="sxs-lookup"><span data-stu-id="fa5cb-124">S3</span></span>
- <span data-ttu-id="fa5cb-125">Режим</span><span class="sxs-lookup"><span data-stu-id="fa5cb-125">S4</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa5cb-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="fa5cb-126">-Tag</span></span>
<span data-ttu-id="fa5cb-127">Указывает тег как пару имя/значение.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-127">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa5cb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa5cb-128">-Confirm</span></span>
<span data-ttu-id="fa5cb-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa5cb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa5cb-130">-WhatIf</span></span>
<span data-ttu-id="fa5cb-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa5cb-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa5cb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa5cb-133">CommonParameters</span></span>
<span data-ttu-id="fa5cb-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa5cb-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa5cb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa5cb-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa5cb-136">INPUTS</span></span>

### <span data-ttu-id="fa5cb-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="fa5cb-137">None</span></span>
<span data-ttu-id="fa5cb-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fa5cb-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa5cb-139">OUTPUTS</span></span>

### <span data-ttu-id="fa5cb-140">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fa5cb-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="fa5cb-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa5cb-141">NOTES</span></span>

## <span data-ttu-id="fa5cb-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa5cb-142">RELATED LINKS</span></span>

[<span data-ttu-id="fa5cb-143">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fa5cb-143">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="fa5cb-144">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fa5cb-144">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="fa5cb-145">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fa5cb-145">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
