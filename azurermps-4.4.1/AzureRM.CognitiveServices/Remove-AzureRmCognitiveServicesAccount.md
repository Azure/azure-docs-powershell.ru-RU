---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a182bed0e93492521e3ac46d5f0ed3e2d705394c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569692"
---
# <span data-ttu-id="975ad-101">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="975ad-101">Remove-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="975ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="975ad-102">SYNOPSIS</span></span>
<span data-ttu-id="975ad-103">Удаление учетной записи службы для восприятия.</span><span class="sxs-lookup"><span data-stu-id="975ad-103">Deletes a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="975ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="975ad-104">SYNTAX</span></span>

```
Remove-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="975ad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="975ad-105">DESCRIPTION</span></span>
<span data-ttu-id="975ad-106">Командлет **Remove-AzureRmCognitiveServicesAccount** удаляет указанную учетную запись службы.</span><span class="sxs-lookup"><span data-stu-id="975ad-106">The **Remove-AzureRmCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="975ad-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="975ad-107">EXAMPLES</span></span>

## <span data-ttu-id="975ad-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="975ad-108">PARAMETERS</span></span>

### <span data-ttu-id="975ad-109">-Force</span><span class="sxs-lookup"><span data-stu-id="975ad-109">-Force</span></span>
<span data-ttu-id="975ad-110">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="975ad-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="975ad-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="975ad-111">-Name</span></span>
<span data-ttu-id="975ad-112">Указывает имя учетной записи, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="975ad-112">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="975ad-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="975ad-113">-ResourceGroupName</span></span>
<span data-ttu-id="975ad-114">Указывает имя группы ресурсов, которой назначена учетная запись службы.</span><span class="sxs-lookup"><span data-stu-id="975ad-114">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="975ad-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="975ad-115">-Confirm</span></span>
<span data-ttu-id="975ad-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="975ad-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="975ad-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="975ad-117">-WhatIf</span></span>
<span data-ttu-id="975ad-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="975ad-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="975ad-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="975ad-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="975ad-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="975ad-120">-DefaultProfile</span></span>
<span data-ttu-id="975ad-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="975ad-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="975ad-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="975ad-122">CommonParameters</span></span>
<span data-ttu-id="975ad-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="975ad-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="975ad-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="975ad-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="975ad-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="975ad-125">INPUTS</span></span>

## <span data-ttu-id="975ad-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="975ad-126">OUTPUTS</span></span>

## <span data-ttu-id="975ad-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="975ad-127">NOTES</span></span>

## <span data-ttu-id="975ad-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="975ad-128">RELATED LINKS</span></span>

[<span data-ttu-id="975ad-129">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="975ad-129">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="975ad-130">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="975ad-130">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="975ad-131">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="975ad-131">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


