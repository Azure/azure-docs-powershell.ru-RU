---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B7E71C5C-6329-475B-993C-A839FFEF8F98
online version: ''
schema: 2.0.0
ms.openlocfilehash: cef5d19cdb954e98fe0e97cc0042bfaf91505c0c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076220"
---
# <span data-ttu-id="9f782-101">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9f782-101">New-AzureAutomationConnection</span></span>

## <span data-ttu-id="9f782-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f782-102">SYNOPSIS</span></span>

<span data-ttu-id="9f782-103">Создает соединение в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="9f782-103">Creates a connection in Automation.</span></span>

## <span data-ttu-id="9f782-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f782-104">SYNTAX</span></span>

```
New-AzureAutomationConnection -Name <String> -ConnectionTypeName <String> -ConnectionFieldValues <IDictionary>
 [-Description <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9f782-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f782-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="9f782-106">Командлет **New-AzureAutomationConnection** создает подключение в службе автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9f782-106">The **New-AzureAutomationConnection** cmdlet creates a connection in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="9f782-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f782-107">EXAMPLES</span></span>

## <span data-ttu-id="9f782-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f782-108">PARAMETERS</span></span>

### <span data-ttu-id="9f782-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9f782-109">-AutomationAccountName</span></span>
<span data-ttu-id="9f782-110">Указывает имя учетной записи автоматизации, в которой будет храниться подключение.</span><span class="sxs-lookup"><span data-stu-id="9f782-110">Specifies the name of the Automation account the connection will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f782-111">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="9f782-111">-ConnectionFieldValues</span></span>
<span data-ttu-id="9f782-112">Указывает хэш-таблицу, которая содержит пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="9f782-112">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="9f782-113">Ключи представляют поля соединения для указанного типа подключения.</span><span class="sxs-lookup"><span data-stu-id="9f782-113">The keys represent the connection fields on the specified connection type.</span></span>
<span data-ttu-id="9f782-114">Значения представляют конкретные значения, которые необходимо сохранить для каждого поля подключения для экземпляра Connection.</span><span class="sxs-lookup"><span data-stu-id="9f782-114">The values represent the specific values to store for each connection field for the connection instance.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f782-115">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="9f782-115">-ConnectionTypeName</span></span>
<span data-ttu-id="9f782-116">Указывает имя типа подключения.</span><span class="sxs-lookup"><span data-stu-id="9f782-116">Specifies the name of the connection type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f782-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="9f782-117">-Description</span></span>
<span data-ttu-id="9f782-118">Задает описание учетных данных.</span><span class="sxs-lookup"><span data-stu-id="9f782-118">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="9f782-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9f782-119">-Name</span></span>
<span data-ttu-id="9f782-120">Задает имя для подключения.</span><span class="sxs-lookup"><span data-stu-id="9f782-120">Specifies a name for the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f782-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="9f782-121">-Profile</span></span>
<span data-ttu-id="9f782-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9f782-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9f782-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9f782-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9f782-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f782-124">CommonParameters</span></span>
<span data-ttu-id="9f782-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f782-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f782-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f782-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f782-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f782-127">INPUTS</span></span>

## <span data-ttu-id="9f782-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f782-128">OUTPUTS</span></span>

### <span data-ttu-id="9f782-129">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="9f782-129">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="9f782-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f782-130">NOTES</span></span>

## <span data-ttu-id="9f782-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f782-131">RELATED LINKS</span></span>

[<span data-ttu-id="9f782-132">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9f782-132">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="9f782-133">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9f782-133">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="9f782-134">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="9f782-134">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


