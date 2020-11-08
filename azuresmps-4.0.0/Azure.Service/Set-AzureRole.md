---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8170AEF9-46E6-4087-8A68-29DFD5D014B5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb63d143ca2cafce92109e17fd3ced6a9dc070e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075824"
---
# <span data-ttu-id="51188-101">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="51188-101">Set-AzureRole</span></span>

## <span data-ttu-id="51188-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51188-102">SYNOPSIS</span></span>
<span data-ttu-id="51188-103">Задает количество экземпляров роли Azure для выполнения.</span><span class="sxs-lookup"><span data-stu-id="51188-103">Sets the number of instances of an Azure role to run.</span></span>

## <span data-ttu-id="51188-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51188-104">SYNTAX</span></span>

```
Set-AzureRole [-ServiceName] <String> [-Slot] <String> [-RoleName] <String> [-Count] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="51188-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51188-105">DESCRIPTION</span></span>
<span data-ttu-id="51188-106">Командлет **Set-AzureRole** задает количество экземпляров указанной роли для выполнения в развертывании Azure.</span><span class="sxs-lookup"><span data-stu-id="51188-106">The **Set-AzureRole** cmdlet sets the number of instances of a specified role to run in an Azure deployment.</span></span>

## <span data-ttu-id="51188-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51188-107">EXAMPLES</span></span>

### <span data-ttu-id="51188-108">1: задание количества экземпляров для роли</span><span class="sxs-lookup"><span data-stu-id="51188-108">1: Set the number of instances for a role</span></span>
```
PS C:\> Set-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestRole03" -Count 3
```

<span data-ttu-id="51188-109">Эта команда задает для роли MyTestRole03, которая выполняется в производстве в службе MySvc01, три экземпляра.</span><span class="sxs-lookup"><span data-stu-id="51188-109">This command sets the MyTestRole03 role that is running in production on the MySvc01 service to have three instances.</span></span>

## <span data-ttu-id="51188-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51188-110">PARAMETERS</span></span>

### <span data-ttu-id="51188-111">— Количество</span><span class="sxs-lookup"><span data-stu-id="51188-111">-Count</span></span>
<span data-ttu-id="51188-112">Указывает количество экземпляров ролей для выполнения.</span><span class="sxs-lookup"><span data-stu-id="51188-112">Specifies the number of role instances to run.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51188-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="51188-113">-InformationAction</span></span>
<span data-ttu-id="51188-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="51188-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="51188-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="51188-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51188-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="51188-116">Continue</span></span>
- <span data-ttu-id="51188-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="51188-117">Ignore</span></span>
- <span data-ttu-id="51188-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="51188-118">Inquire</span></span>
- <span data-ttu-id="51188-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="51188-119">SilentlyContinue</span></span>
- <span data-ttu-id="51188-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="51188-120">Stop</span></span>
- <span data-ttu-id="51188-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="51188-121">Suspend</span></span>

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

### <span data-ttu-id="51188-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="51188-122">-InformationVariable</span></span>
<span data-ttu-id="51188-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="51188-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="51188-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="51188-124">-Profile</span></span>
<span data-ttu-id="51188-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="51188-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51188-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51188-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51188-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="51188-127">-RoleName</span></span>
<span data-ttu-id="51188-128">Указывает имя роли, для которой задается количество экземпляров.</span><span class="sxs-lookup"><span data-stu-id="51188-128">Specifies the name of the role for which to set the number of instances.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51188-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="51188-129">-ServiceName</span></span>
<span data-ttu-id="51188-130">Указывает имя службы Azure.</span><span class="sxs-lookup"><span data-stu-id="51188-130">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="51188-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="51188-131">-Slot</span></span>
<span data-ttu-id="51188-132">Указывает среду развертывания для развертывания, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="51188-132">Specifies the deployment environment of the deployment to modify.</span></span>
<span data-ttu-id="51188-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="51188-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51188-134">Спецификации</span><span class="sxs-lookup"><span data-stu-id="51188-134">Production</span></span>
- <span data-ttu-id="51188-135">Промежуточного хранения</span><span class="sxs-lookup"><span data-stu-id="51188-135">Staging</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51188-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51188-136">CommonParameters</span></span>
<span data-ttu-id="51188-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51188-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51188-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51188-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51188-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51188-139">INPUTS</span></span>

## <span data-ttu-id="51188-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51188-140">OUTPUTS</span></span>

## <span data-ttu-id="51188-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="51188-141">NOTES</span></span>

## <span data-ttu-id="51188-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51188-142">RELATED LINKS</span></span>

[<span data-ttu-id="51188-143">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="51188-143">Get-AzureRole</span></span>](./Get-AzureRole.md)


