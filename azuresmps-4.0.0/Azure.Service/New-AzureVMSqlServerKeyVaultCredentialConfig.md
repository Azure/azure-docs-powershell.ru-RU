---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EC6F7790-5E31-4C22-B006-38B5C1868671
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0272740ced33d19e2610a6116812df4a815ea3c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076188"
---
# <span data-ttu-id="1569a-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="1569a-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="1569a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1569a-102">SYNOPSIS</span></span>

## <span data-ttu-id="1569a-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1569a-103">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-Enable] [[-CredentialName] <String>]
 [[-AzureKeyVaultUrl] <String>] [[-ServicePrincipalName] <String>] [[-ServicePrincipalSecret] <SecureString>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="1569a-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1569a-104">DESCRIPTION</span></span>

## <span data-ttu-id="1569a-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1569a-105">EXAMPLES</span></span>

### <span data-ttu-id="1569a-106">1:</span><span class="sxs-lookup"><span data-stu-id="1569a-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="1569a-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1569a-107">PARAMETERS</span></span>

### <span data-ttu-id="1569a-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="1569a-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1569a-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="1569a-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1569a-110">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="1569a-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1569a-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1569a-111">-InformationAction</span></span>
<span data-ttu-id="1569a-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="1569a-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1569a-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1569a-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1569a-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="1569a-114">Continue</span></span>
- <span data-ttu-id="1569a-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="1569a-115">Ignore</span></span>
- <span data-ttu-id="1569a-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="1569a-116">Inquire</span></span>
- <span data-ttu-id="1569a-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1569a-117">SilentlyContinue</span></span>
- <span data-ttu-id="1569a-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="1569a-118">Stop</span></span>
- <span data-ttu-id="1569a-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="1569a-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1569a-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1569a-120">-InformationVariable</span></span>
<span data-ttu-id="1569a-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="1569a-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1569a-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="1569a-122">-Profile</span></span>
```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1569a-123">-Намерено</span><span class="sxs-lookup"><span data-stu-id="1569a-123">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1569a-124">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="1569a-124">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1569a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1569a-125">CommonParameters</span></span>
<span data-ttu-id="1569a-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1569a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1569a-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1569a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1569a-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1569a-128">INPUTS</span></span>

## <span data-ttu-id="1569a-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1569a-129">OUTPUTS</span></span>

## <span data-ttu-id="1569a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="1569a-130">NOTES</span></span>

## <span data-ttu-id="1569a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1569a-131">RELATED LINKS</span></span>

