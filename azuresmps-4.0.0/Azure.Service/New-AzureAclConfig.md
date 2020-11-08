---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CD2274E5-B3D4-489E-B374-8B2BCC1F923E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90666be18ee3e546620d0c10386594b8ae7ec8a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076235"
---
# <span data-ttu-id="0d03d-101">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="0d03d-101">New-AzureAclConfig</span></span>

## <span data-ttu-id="0d03d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d03d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d03d-103">Создание пустого объекта конфигурации ACL.</span><span class="sxs-lookup"><span data-stu-id="0d03d-103">Creates an empty ACL configuration object.</span></span>

## <span data-ttu-id="0d03d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d03d-104">SYNTAX</span></span>

```
New-AzureAclConfig [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0d03d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d03d-105">DESCRIPTION</span></span>
<span data-ttu-id="0d03d-106">Командлет **New-AzureAclConfig** создает пустой объект конфигурации списка управления доступом (ACL).</span><span class="sxs-lookup"><span data-stu-id="0d03d-106">The **New-AzureAclConfig** cmdlet creates an empty access control list (ACL) configuration object.</span></span>

## <span data-ttu-id="0d03d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d03d-107">EXAMPLES</span></span>

### <span data-ttu-id="0d03d-108">Пример 1: создание объекта конфигурации ACL</span><span class="sxs-lookup"><span data-stu-id="0d03d-108">Example 1: Create an ACL configuration object</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
```

<span data-ttu-id="0d03d-109">Эта команда создает пустой объект конфигурации ACL и сохраняет его в переменной $Acl.</span><span class="sxs-lookup"><span data-stu-id="0d03d-109">This command creates an empty ACL configuration object, and then stores it in the $Acl variable.</span></span>

## <span data-ttu-id="0d03d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d03d-110">PARAMETERS</span></span>

### <span data-ttu-id="0d03d-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0d03d-111">-InformationAction</span></span>
<span data-ttu-id="0d03d-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="0d03d-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0d03d-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0d03d-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d03d-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="0d03d-114">Continue</span></span>
- <span data-ttu-id="0d03d-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="0d03d-115">Ignore</span></span>
- <span data-ttu-id="0d03d-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="0d03d-116">Inquire</span></span>
- <span data-ttu-id="0d03d-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0d03d-117">SilentlyContinue</span></span>
- <span data-ttu-id="0d03d-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="0d03d-118">Stop</span></span>
- <span data-ttu-id="0d03d-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="0d03d-119">Suspend</span></span>

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

### <span data-ttu-id="0d03d-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0d03d-120">-InformationVariable</span></span>
<span data-ttu-id="0d03d-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="0d03d-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0d03d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d03d-122">CommonParameters</span></span>
<span data-ttu-id="0d03d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d03d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d03d-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d03d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d03d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d03d-125">INPUTS</span></span>

## <span data-ttu-id="0d03d-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d03d-126">OUTPUTS</span></span>

## <span data-ttu-id="0d03d-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d03d-127">NOTES</span></span>

## <span data-ttu-id="0d03d-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d03d-128">RELATED LINKS</span></span>

[<span data-ttu-id="0d03d-129">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="0d03d-129">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="0d03d-130">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="0d03d-130">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="0d03d-131">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="0d03d-131">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


