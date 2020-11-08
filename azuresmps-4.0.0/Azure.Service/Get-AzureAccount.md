---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 70ADAF16-BC52-47BF-A85A-A84DEACDA027
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2704dbdc308b9773452b05ceba24719f2e274132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075676"
---
# <span data-ttu-id="6fd64-101">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="6fd64-101">Get-AzureAccount</span></span>

## <span data-ttu-id="6fd64-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6fd64-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd64-103">Возвращает учетные записи Azure, доступные для Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6fd64-103">Gets Azure accounts that are available to Azure PowerShell.</span></span>

## <span data-ttu-id="6fd64-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6fd64-104">SYNTAX</span></span>

```
Get-AzureAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6fd64-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fd64-105">DESCRIPTION</span></span>
<span data-ttu-id="6fd64-106">Командлет **Get-AzureAccount** получает учетные записи Azure, доступные для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6fd64-106">The **Get-AzureAccount** cmdlet gets the Azure accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="6fd64-107">Чтобы сделать учетные записи доступными для Windows PowerShell, используйте командлеты **Add-AzureAccount** или **Import-PublishSettingsFile** .</span><span class="sxs-lookup"><span data-stu-id="6fd64-107">To make your accounts available to Windows PowerShell, use the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="6fd64-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6fd64-108">EXAMPLES</span></span>

### <span data-ttu-id="6fd64-109">Пример 1: получение всех учетных записей</span><span class="sxs-lookup"><span data-stu-id="6fd64-109">Example 1: Get all accounts</span></span>
```
PS C:\> Get-AzureAccount

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
contosotest1@outlook.com     {{ ActiveDirectoryTenantId = aaeabcde-386c-4466-bf70-794...
```

<span data-ttu-id="6fd64-110">Эта команда возвращает все учетные записи, связанные с указанным пользователем.</span><span class="sxs-lookup"><span data-stu-id="6fd64-110">This command gets all accounts associated with the specified user.</span></span>

### <span data-ttu-id="6fd64-111">Пример 2: получение учетной записи по имени</span><span class="sxs-lookup"><span data-stu-id="6fd64-111">Example 2: Get an account by name</span></span>
```
PS C:\> Get-AzureAccount -Name contosoadmin@outlook.com

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
```

<span data-ttu-id="6fd64-112">Эта команда получает учетную запись ContosoAdmin.</span><span class="sxs-lookup"><span data-stu-id="6fd64-112">This command gets the ContosoAdmin account.</span></span>

## <span data-ttu-id="6fd64-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6fd64-113">PARAMETERS</span></span>

### <span data-ttu-id="6fd64-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6fd64-114">-Name</span></span>
<span data-ttu-id="6fd64-115">Возвращает только указанную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="6fd64-115">Gets only the specified account.</span></span>
<span data-ttu-id="6fd64-116">По умолчанию все учетные записи доступны для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6fd64-116">The default is all accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="6fd64-117">Введите имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6fd64-117">Enter the account name.</span></span>
<span data-ttu-id="6fd64-118">Значение **Name** задается с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="6fd64-118">The **Name** value is case-sensitive.</span></span>
<span data-ttu-id="6fd64-119">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="6fd64-119">Wildcards are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd64-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="6fd64-120">-Profile</span></span>
<span data-ttu-id="6fd64-121">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6fd64-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6fd64-122">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6fd64-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6fd64-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd64-123">CommonParameters</span></span>
<span data-ttu-id="6fd64-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6fd64-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd64-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fd64-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd64-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6fd64-126">INPUTS</span></span>

### <span data-ttu-id="6fd64-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="6fd64-127">None</span></span>
<span data-ttu-id="6fd64-128">Вы не можете передавать входные данные в этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6fd64-128">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="6fd64-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fd64-129">OUTPUTS</span></span>

### <span data-ttu-id="6fd64-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="6fd64-130">None</span></span>
<span data-ttu-id="6fd64-131">Этот командлет не возвращает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6fd64-131">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="6fd64-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="6fd64-132">NOTES</span></span>

## <span data-ttu-id="6fd64-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6fd64-133">RELATED LINKS</span></span>

[<span data-ttu-id="6fd64-134">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="6fd64-134">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="6fd64-135">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="6fd64-135">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="6fd64-136">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="6fd64-136">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="6fd64-137">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="6fd64-137">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


