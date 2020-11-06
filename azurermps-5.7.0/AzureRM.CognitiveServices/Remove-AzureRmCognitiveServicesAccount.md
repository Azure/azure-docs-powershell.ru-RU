---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/remove-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 7c77f11842c224a0a023215175f52bf451867296
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568637"
---
# <span data-ttu-id="a4dd7-101">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a4dd7-101">Remove-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="a4dd7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="a4dd7-103">Удаление учетной записи службы для восприятия.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-103">Deletes a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4dd7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4dd7-104">SYNTAX</span></span>

```
Remove-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4dd7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4dd7-105">DESCRIPTION</span></span>
<span data-ttu-id="a4dd7-106">Командлет **Remove-AzureRmCognitiveServicesAccount** удаляет указанную учетную запись службы.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-106">The **Remove-AzureRmCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="a4dd7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4dd7-107">EXAMPLES</span></span>

## <span data-ttu-id="a4dd7-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4dd7-108">PARAMETERS</span></span>

### <span data-ttu-id="a4dd7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4dd7-109">-DefaultProfile</span></span>
<span data-ttu-id="a4dd7-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a4dd7-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4dd7-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a4dd7-111">-Force</span></span>
<span data-ttu-id="a4dd7-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4dd7-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a4dd7-113">-Name</span></span>
<span data-ttu-id="a4dd7-114">Указывает имя учетной записи, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-114">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="a4dd7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4dd7-115">-ResourceGroupName</span></span>
<span data-ttu-id="a4dd7-116">Указывает имя группы ресурсов, которой назначена учетная запись службы.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-116">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="a4dd7-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4dd7-117">-Confirm</span></span>
<span data-ttu-id="a4dd7-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4dd7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4dd7-119">-WhatIf</span></span>
<span data-ttu-id="a4dd7-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4dd7-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4dd7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4dd7-122">CommonParameters</span></span>
<span data-ttu-id="a4dd7-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4dd7-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4dd7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4dd7-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4dd7-125">INPUTS</span></span>

### <span data-ttu-id="a4dd7-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="a4dd7-126">None</span></span>
<span data-ttu-id="a4dd7-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a4dd7-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4dd7-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4dd7-128">OUTPUTS</span></span>

## <span data-ttu-id="a4dd7-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4dd7-129">NOTES</span></span>

## <span data-ttu-id="a4dd7-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4dd7-130">RELATED LINKS</span></span>

[<span data-ttu-id="a4dd7-131">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a4dd7-131">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="a4dd7-132">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a4dd7-132">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="a4dd7-133">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a4dd7-133">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


